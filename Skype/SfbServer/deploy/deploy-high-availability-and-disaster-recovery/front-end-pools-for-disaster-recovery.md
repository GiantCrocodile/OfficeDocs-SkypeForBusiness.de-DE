---
title: Bereitstellen von Front-End-Poolpaaren für die Notfallwiederherstellung in Skype for Business Server 2015
ms.author: heidip
author: microsoftheidi
manager: serdars
ms.date: 9/1/2016
ms.audience: ITPro
ms.topic: get-started-article
ms.prod: skype-for-business-itpro
localization_priority: Normal
ms.assetid: 2f12467c-8b90-43e6-831b-a0b096427f17
description: Sie können Front-End-Poolpaare verwenden, um Schutz durch Notfallwiederherstellung bereitzustellen. Dies ist jedoch nicht erforderlich.
ms.openlocfilehash: e13694c364908cfef70edafc1e7eb0484c5fe1bd
ms.sourcegitcommit: 7d819bc9eb63bfd85f5dada09f1b8e5354c56f6b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2018
---
# <a name="deploy-paired-front-end-pools-for-disaster-recovery-in-skype-for-business-server-2015"></a>Bereitstellen von Front-End-Poolpaaren für die Notfallwiederherstellung in Skype for Business Server 2015
 
Sie können Front-End-Poolpaare verwenden, um Schutz durch Notfallwiederherstellung bereitzustellen. Dies ist jedoch nicht erforderlich.
  
Sie können die notfallwiederherstellungstopologie eines Paars Front-End-Pools des Topologie-Generators auf einfache Weise bereitstellen. 
  
## <a name="to-deploy-a-pair-of-front-end-pools"></a>So stellen Sie ein Front-End-Poolpaar bereit

1. Wenn die Pools neu und noch nicht definiert sind, verwenden Sie zum Erstellen der Pools Topologie-Generator.
    
2. Klicken Sie im Topologie-Generator Maustaste auf eine der beiden Pools, und klicken Sie dann auf **Eigenschaften bearbeiten**.
    
3. Klicken Sie im linken Bereich auf **Flexibilität**, und wählen Sie dann im rechten Bereich die Option **Zugeordneter Sicherungspool** aus.
    
4. Wählen Sie im Feld unter **Zugeordneter Sicherungspool** den Pool aus, mit dem dieser Pool ein Paar bilden soll. Zur Auswahl stehen nur vorhandene Pools, die noch nicht mit einem anderen Pool ein Paar bilden.
    
5. Wählen Sie **Automatisches Failover und Failback für Sprachdienste** aus, und klicken Sie dann auf **OK**.
    
    Wenn Sie die Details zu diesem Pool anzeigen, erscheint der zugeordnete Pool jetzt im rechten Bereich unter **Flexibilität**.  
    
6. Verwenden Sie zum Veröffentlichen der Topologie Topologie-Generator.
    
7. Wenn die beiden Pools noch nicht bereitgestellt wurden, führen Sie die Bereitstellung jetzt durch, um die Konfiguration abzuschließen. Die letzten beiden Schritte in diesem Verfahren können Sie überspringen.
    
    Wenn die Pools jedoch bereits bereitgestellt waren, bevor Sie die Paarbeziehung definiert haben, müssen Sie die beiden folgenden abschließenden Schritte ausführen.
    
8. Führen Sie auf jedem Front-End-Server in beiden Pools Folgendes aus:
    
   ```
   <system drive>\Program Files\Skype for Business Server 2015\Deployment\Bootstrapper.exe 
   ```

    Hierdurch werden die anderen Dienste konfiguriert, die erforderlich sind, damit die Sicherung des Poolpaars korrekt funktioniert.
    
9. Führen Sie aus einer Skype für Business Server-Verwaltungsshell an der Eingabeaufforderung folgenden Befehl: 
    
   ```
   Start-CsWindowsService -Name LYNCBACKUP
   ```

10. Verwenden Sie die folgenden Cmdlets, um zu erzwingen, dass die Benutzer- und Konferenzdaten beider Pools miteinander synchronisiert werden:
    
   ```
   Invoke-CsBackupServiceSync -PoolFqdn <Pool1 FQDN>
   ```

   ```
   Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN>
   ```

   Das Synchronisieren der Daten kann einige Zeit in Anspruch nehmen. Sie können die folgenden Cmdlets verwenden, um den Status zu überprüfen. Stellen Sie sicher, dass der Status für beide Richtungen stabil ist.
    
   ```
   Get-CsBackupServiceStatus -PoolFqdn <Pool1 FQDN>
   ```

   ```
   Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN>
   ```

> [!NOTE]
> Die Option **Automatisches Failover und Failback für VoIP** und die zugehörigen Zeitintervalle im Topologie-Generator gelten nur für die VoIP-ausfallsicherheit-Funktionen, die in Lync Server eingeführt wurden. Durch Auswählen dieser Option impliziert nicht, dass die in diesem Dokument beschriebenen poolfailover automatisch erfolgt. Failover und Failback müssen immer ein Administrator manuell die Cmdlets Failover und Failback jeweils aufrufen.
  
## <a name="see-also"></a>Siehe auch

#### 

[Front-End-Pool Disaster Recovery in Skype für Business Server 2015](../../plan-your-deployment/high-availability-and-disaster-recovery/disaster-recovery.md)

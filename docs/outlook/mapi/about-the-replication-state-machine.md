---
title: Informationen über den Replikationszustandsautomaten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 30dd43a3ac9a315cd41919872b918bee639ca259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593053"
---
# <a name="about-the-replication-state-machine"></a>Informationen über den Replikationszustandsautomaten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält eine Übersicht über die Zustandsautomat für die Datenreplikation für Microsoft Outlook 2013 und Microsoft Outlook 2010.
  
> [!NOTE]
> Die Replikation API muss gemäß den Anweisungen in diesem Thema, um die Benutzer nützlich oder unterstützte vollständig implementiert werden. Die Replikation-API ist ausschließlich für Outlook 2013 oder Outlook 2010 Änderungen an und von einem Server zu replizieren verfügbar. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX und der Zustandsautomat

Ein Client ruft **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** und **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** in einer Sequenz zum Synchronisieren von Outlook 2013 oder Outlook 2010-Ordner und Elemente zwischen einer lokalen Speicher und einem Server. Die tatsächlichen Folge der Aufrufe hängt die Daten, die auf (z. B., eine Hierarchie von Ordnern für Outlook 2013 oder Outlook 2010, ein Outlook 2013 oder Outlook 2010-Ordner, e-Mail-Elementen, Kalenderelemente und usw.) repliziert werden müssen und die Richtung der Synchronisierung (, ob Hochladen aus dem lokalen Speicher auf dem Server oder auf den lokalen Speicher vom Server herunterladen). Hier ist eine typische Folge der Aufrufe aus: 
  
1. Der Client ruft **IOSTX::SyncBeg** Replikation beginnen, um einen Bezeichner Zustand und einen Zeiger auf eine Adresse einer entsprechenden Datenstruktur angeben. 
    
2. Outlook 2013 oder Outlook 2010 weist die Datenstruktur und initialisiert die Datenstruktur mit den erforderlichen Informationen für den Client. 
    
3. Der Client führt die Replikation aktualisieren die Datenstruktur, um alle erforderlichen Informationen über die Replikation auf den lokalen Speicher zu vermitteln.
    
4. Nach dem Ausführen der Replikations, ruft der Client **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** und **IOSTX::SyncEnd** , um den lokalen Speicher nach Abschluss der bestimmten Replikation zu benachrichtigen. 
    
> [!NOTE]
> Der Client ruft immer **IOSTX::SyncEnd** , um eine Replikation zu beenden, die der Client für einen bestimmten Zustand begonnen hat. Je nach der gesamten Daten, die der Client synchronisieren muss, kann der Client die beiden Anrufe **IOSTX::SyncBeg** und **IOSTX::SyncEnd** nur einmal aufrufen. 
  
## <a name="state-table"></a>State-Tabelle

> [!NOTE]
> Die folgende Tabelle enthält die gültigen Zustände in der Zustandsautomat Replikation zusammen mit den entsprechenden Status Bezeichner und Datenstrukturen. In der Spalte **Daten repliziert** enthält der Begriff "Elemente" e-Mail, Kalender, Kontakt, Notizen, Journal und Aufgabenelementen. Beim Replizieren von Änderungen aus dem lokalen Speicher auf dem Server, verwenden Sie die State-IDs angeben "Hochladen" und Datenstrukturen mit dem "Nach oben" Präfix (z. B. **LR_SYNC_UPLOAD_HIERARCHY** und **[UPHIER](uphier.md)** ). Beim Replizieren von Änderungen vom Server auf den lokalen Speicher, verwenden Sie die State-IDs angeben "Herunterladen" und Datenstrukturen mit dem Präfix "DN" (beispielsweise **LR_SYNC_DOWNLOAD_HIERARCHY** und **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Replizierten Daten** <br/> |**State-ID** <br/> |**Datenstruktur** <br/> |
|[Leerlauf](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Synchronisieren von Zustand](synchronize-state.md) <br/> |Ordner oder Elemente  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Hochladen der Hierarchie Zustand](upload-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Ordner Zustand hochladen](upload-folder-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchronisieren von Inhalt Zustand](synchronize-contents-state.md) <br/> |Elemente  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Tabelle Zustand hochladen](upload-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Nachrichtenstatus hochladen](upload-message-state.md) <br/> |Element  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Upload Status Zustand lesen](upload-read-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Status-Status löschen hochladen](upload-delete-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Hierarchie Downloadstatus](download-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Tabelle Downloadstatus](download-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md) <br/> |Nachrichtenkopf  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Statusübergang-Diagramm

Das folgende Diagramm zeigt die Statusübergänge, die beim Hochladen oder das Ausführen einer vollständigen Synchronisierung (Download gefolgt von hochladen) von Ordnern oder Inhalt von Ordnern (e-Mail, Kalender, Kontakt, Notiz, Aufgabe oder Journalelemente) auftreten. 
  
@@@NEED AUF GRAFIK EINFÜGEN HIER, DER FEHLT @@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Beispiel: Hochladen einer Ordnerhierarchie

 Beim Hochladen einer Hierarchie von Ordnern erfolgt die folgende Schrittfolge: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Schritt** <br/> |**Aktion** <br/> |**State** <br/> |**Verwandte-Datenstruktur** <br/> |
|1.  <br/> |Den Upload Hierarchie mit **IOSTX::SyncBeg**wird vom Client initiiert.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPHIER** mit Informationen für den Client. Dazu gehören die [Out]-Parameter initialisieren: *iEnt* auf 0 und *cEnt* auf die Anzahl der Ordner in der Hierarchie, das Hochladen von benötigt festgelegt ist.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Der Client führt das tatsächliche Hierarchie hochladen. Als Beispiel *cEnt* 10, für jeden der 10 Ordner ist, ruft der Client **IOSTX::SyncBeg**, den entsprechenden Statusbezeichner und die Datenstruktur zum Hochladen eines Ordners angeben.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPFLD** [Out] Parameter, einschließlich der Grund für den Ordner Upload, den Zeiger auf das Folder-Objekt und die Eintrags-ID für den Ordner zu initialisieren.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Der Client hochgeladen im angegebenen Ordner.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Der Client benachrichtigt den lokalen Speicher nach Abschluss des Uploads Ordner: bei Erfolg der Client legt fest, die [in] Parameter *UlFlags* in **UPFLD** mit **UPF_OK**, und klicken Sie dann auf Anrufe **IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd **. Bei Auftreten eines Fehlers würde der Client nicht *UlFlags* mit dem **UPF_OK** -Flag festgelegt. Sie ruft **IOSTX::SetSyncResult**, in der **HRESULT** -Wert und **IOSTX::SyncEnd**übergeben.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Wenn **UPF_OK** festgelegt ist, wird die interne Anforderung für den Ordner hochladen Outlook 2013 oder Outlook 2010 gelöscht werden. Klicken Sie dann unabhängig von der Einstellung *UlFlags* bereinigt sie alle internen Protokollinformationen. Während es noch Ordner in der Hierarchie sind Hochladen (*iEnt* ist weiterhin kleiner als *cEnt*), den Client und Outlook 2013 oder Outlook 2010 wiederholen Sie die Schritte 3 bis 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Der Client benachrichtigt den lokalen Speicher nach Abschluss des Uploads Hierarchie: bei Erfolg der Client legt fest, die [in] **IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd**-flag in **UPHIER** mit **UPH_OK**, und dann wird. Bei Auftreten eines Fehlers würde der Client nicht das Flag **UPH_OK** festgelegt. Sie ruft **IOSTX::SetSyncResult**, in der **HRESULT** -Wert und **IOSTX::SyncEnd**übergeben.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Wenn **UPH_OK** festgelegt ist, wird die interne Anforderung zum Hochladen der Hierarchie Outlook 2013 oder Outlook 2010 gelöscht werden. Klicken Sie dann unabhängig von der Einstellung *UlFlags* bereinigt sie alle internen Protokollinformationen.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)


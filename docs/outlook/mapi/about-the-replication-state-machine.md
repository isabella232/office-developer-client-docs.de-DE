---
title: Informationen über den Replikationszustandsautomaten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0644e4bf5c6847d61cc59e203d50f61ad142e84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416482"
---
# <a name="about-the-replication-state-machine"></a>Informationen über den Replikationszustandsautomaten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält eine Übersicht über den Statuscomputer für Microsoft Outlook 2013 und Microsoft Outlook 2010 Datenreplikation.
  
> [!NOTE]
> Die Replikations-API muss gemäß den Anweisungen in diesem Thema vollständig implementiert werden, um nützlich oder unterstützt zu werden. Die Replikations-API steht ausschließlich zum Replizieren Outlook 2013 oder Outlook 2010-Änderungen auf und von einem Server zur Verfügung. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX und der Zustandsautomat

Ein Client ruft **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** und **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** in einer Sequenz auf, um Ordner und Elemente von Outlook 2013 oder Outlook 2010 zwischen einem lokalen Speicher und einem Server zu synchronisieren. Die tatsächliche Reihenfolge der Aufrufe hängt von den Daten ab, die repliziert werden müssen (z. B. eine Hierarchie von Outlook 2013- oder Outlook 2010-Ordnern, einem Ordner Outlook 2013 oder Outlook 2010, E-Mail-Elementen, Kalenderelementen und so weiter) und der Richtung der Synchronisierung (ob das Hochladen vom lokalen Speicher auf den Server oder das Herunterladen vom Server in den lokalen Speicher). Dies ist eine typische Abfolge von Aufrufen: 
  
1. Der Client ruft **IOSTX::SyncBeg** auf, um mit der Replikation zu beginnen, und gibt einen Statusbezeichner und einen Zeiger auf eine Adresse einer entsprechenden Datenstruktur an. 
    
2. Outlook 2013 oder Outlook 2010 wird die Datenstruktur zugewiesen und die Datenstruktur mit den erforderlichen Informationen für den Client initialisiert. 
    
3. Der Client führt die Replikation durch und aktualisiert die Datenstruktur, um alle erforderlichen Informationen zur Replikation an den lokalen Speicher zu übermitteln.
    
4. Nach der Replikation ruft der Client **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** und **IOSTX::SyncEnd** auf, um den lokalen Speicher über den Abschluss der spezifischen Replikation zu benachrichtigen. 
    
> [!NOTE]
> Der Client ruft immer **IOSTX::SyncEnd auf,** um eine Replikation zu beenden, die der Client für einen bestimmten Zustand gestartet hat. Abhängig von den Gesamtdaten, die der Client synchronisieren muss, kann der Client das Anrufpaar **IOSTX::SyncBeg** und **IOSTX::SyncEnd** mehr als einmal aufrufen. 
  
## <a name="state-table"></a>Statustabelle

> [!NOTE]
> In der folgenden Tabelle sind alle gültigen Zustände auf dem Replikationsstatuscomputer sowie die entsprechenden Statusbezeichner und Datenstrukturen aufgeführt. In der **Spalte Daten repliziert** umfasst der Begriff "Elemente" E-Mail, Kalender, Kontakt, Notiz, Journal und Aufgabenelemente. Verwenden Sie beim Replizieren von Änderungen vom lokalen Speicher auf den Server Statusbezeichner, die "UPLOAD" angeben, und Datenstrukturen mit dem Präfix "UP" (z. B. **LR_SYNC_UPLOAD_HIERARCHY** **[und UPHIER](uphier.md)** ). Verwenden Sie beim Replizieren von Änderungen vom Server in den lokalen Speicher Statusbezeichner, die "DOWNLOAD" angeben, und Datenstrukturen mit dem Präfix "DN" (z. B. **LR_SYNC_DOWNLOAD_HIERARCHY** und **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Replizierte Daten** <br/> |**Statusbezeichner** <br/> |**Datenstruktur** <br/> |
|[Zustand „Leerlauf“](idle-state.md) <br/> | *Keine*  <br/> |**LR_SYNC_IDLE** <br/> | *Keine*  <br/> |
|[Zustand „Synchronisieren“](synchronize-state.md) <br/> |Ordner oder Elemente  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Hochladen Hierarchiestatus](upload-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Hochladen Ordnerstatus](upload-folder-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchronisieren des Inhaltszustands](synchronize-contents-state.md) <br/> |Elemente  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Hochladen Tabellenstatus](upload-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Hochladen Nachrichtenstatus](upload-message-state.md) <br/> |Element  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Hochladen Statusstatus lesen](upload-read-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Hochladen Statusstatus löschen](upload-delete-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Hierarchiestatus herunterladen](download-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Tabellenstatus herunterladen](download-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Nachrichtenkopfstatus herunterladen](download-message-header-state.md) <br/> |Nachrichtenkopf  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Zustandsübergangsdiagramm

Das folgende Diagramm zeigt die Statusübergänge, die beim Hochladen oder Ausführen einer vollständigen Synchronisierung (Herunterladen gefolgt von dem Hochladen) von Ordnern oder Inhalten von Ordnern (E-Mail, Kalender, Kontakt, Hinweis, Aufgabe oder Journalelemente) auftreten. 
  
@@@@@NEED, UM HIER FEHLENDES BILD EINFÜGEN @@@@@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Beispiel: Hochladen einer Ordnerhierarchie

 Beim Hochladen einer Hierarchie von Ordnern erfolgt die folgende Abfolge von Schritten: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Schritt** <br/> |**Aktion** <br/> |**State** <br/> |**Verwandte Datenstruktur** <br/> |
|1.  <br/> |Der Client initiiert den Hierarchieupload mit **IOSTX::SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPHIER** mit Informationen für den Client. Dies umfasst das Initialisieren der [out]-Parameter:  *iEnt*  ist auf 0 festgelegt, und  *cEnt*  auf die Anzahl der Ordner in der Hierarchie, die hochgeladen werden muss.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Der Client führt den tatsächlichen Hierarchieupload durch. Wenn  *cEnt*  z. B. 10 ist, ruft der Client für jeden der 10 Ordner **IOSTX::SyncBeg** auf, um den entsprechenden Statusbezeichner und die Datenstruktur für das Hochladen eines Ordners anzugeben.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPFLD** auf, indem seine [out]-Parameter initialisiert werden, einschließlich des Grunds für den Ordnerupload, des Zeigers auf das Ordnerobjekt und der Eintrags-ID für den Ordner.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Der Client lädt den angegebenen Ordner hoch.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Ordneruploads: Bei erfolgreichem Abschluss legt der Client den [in]-Parameter  *ulFlags*  in **UPFLD** mit **UPF_OK** fest und ruft **dann IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd** auf. Bei einem Fehler würde der Client *ulFlags* nicht mit dem UPF_OK **festlegen.** Es ruft **IOSTX::SetSyncResult auf,** und gibt den **HRESULT-Wert** und **IOSTX::SyncEnd an.**  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Wenn **UPF_OK** festgelegt ist, Outlook 2013 oder Outlook 2010 die interne Anforderung zum Hochladen des Ordners löschen. Unabhängig vom Status von  *ulFlags*  werden dann alle internen Buchhaltungsinformationen bereinigt. Während in der Hierarchie noch Ordner hochgeladen werden sollen *(iEnt* ist immer noch kleiner als *cEnt),* wiederholen der Client und Outlook 2013 oder Outlook 2010 die Schritte 3 bis 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Hierarchieuploads: Bei Erfolg legt der Client das Flag [in] in **UPHIER** mit **UPH_OK** fest und ruft **dann IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd auf.** Bei einem Fehler würde der Client das UPH_OK **festlegen.** Es ruft **IOSTX::SetSyncResult auf,** und gibt den **HRESULT-Wert** und **IOSTX::SyncEnd an.**  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Wenn **UPH_OK** festgelegt ist, Outlook 2013 oder Outlook 2010 die interne Anforderung zum Hochladen der Hierarchie löschen. Unabhängig vom Status von  *ulFlags*  werden dann alle internen Buchhaltungsinformationen bereinigt.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)


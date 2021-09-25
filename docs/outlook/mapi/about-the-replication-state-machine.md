---
title: Informationen über den Replikationszustandsautomaten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c0f0f61c53fa868bfabd29cdb3cfaf278bcd846d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564484"
---
# <a name="about-the-replication-state-machine"></a>Informationen über den Replikationszustandsautomaten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält eine Übersicht über den Zustandsautomaten für Microsoft Outlook 2013 und Microsoft Outlook 2010 Datenreplikation.
  
> [!NOTE]
> Die Replikations-API muss gemäß den Anweisungen in diesem Thema vollständig implementiert werden, damit sie nützlich oder unterstützt wird. Die Replikations-API ist exklusiv verfügbar, um Outlook 2013- oder Outlook 2010-Änderungen an und von einem Server zu replizieren. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX und der Zustandsautomat

Ein Client ruft **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** und **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** in einer Sequenz auf, um Outlook 2013- oder Outlook 2010-Ordner und Elemente zwischen einem lokalen Speicher und einem Server zu synchronisieren. Die tatsächliche Abfolge von Aufrufen hängt von den Daten ab, die repliziert werden müssen (z. B. eine Hierarchie der Ordner Outlook 2013 oder Outlook 2010, ein ordner Outlook 2013 oder Outlook 2010, E-Mail-Elemente, Kalenderelemente usw.) und die Synchronisierungsrichtung (ob hochladen aus dem lokalen Speicher auf den Server oder Herunterladen vom Server in den lokalen Speicher). Nachfolgend finden Sie eine typische Abfolge von Aufrufen: 
  
1. Der Client ruft **IOSTX::SyncBeg** auf, um mit der Replikation zu beginnen, und gibt einen Statusbezeichner und einen Zeiger auf eine Adresse einer entsprechenden Datenstruktur an. 
    
2. Outlook 2013 oder Outlook 2010 ordnet die Datenstruktur zu und initialisiert die Datenstruktur mit den erforderlichen Informationen für den Client. 
    
3. Der Client führt die Replikation durch und aktualisiert die Datenstruktur, um dem lokalen Speicher alle erforderlichen Informationen zur Replikation zu übermitteln.
    
4. Nach dem Ausführen der Replikation ruft der Client **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** und **IOSTX::SyncEnd** auf, um den lokalen Speicher über den Abschluss der spezifischen Replikation zu benachrichtigen. 
    
> [!NOTE]
> Der Client ruft immer **IOSTX::SyncEnd** auf, um eine Replikation zu beenden, die der Client für einen bestimmten Zustand begonnen hat. Abhängig von den Gesamtdaten, die der Client synchronisieren muss, kann der Client das Anrufpaar **IOSTX::SyncBeg** und **IOSTX::SyncEnd mehrmals** aufrufen. 
  
## <a name="state-table"></a>State-Tabelle

> [!NOTE]
> In der folgenden Tabelle sind alle gültigen Zustände auf dem Replikationsstatuscomputer sowie die entsprechenden Statusbezeichner und Datenstrukturen aufgeführt. In der Spalte **"Datenreplikation"** enthält der Begriff "Elemente" E-Mail-, Kalender-, Kontakt-, Notiz-, Journal- und Aufgabenelemente. Verwenden Sie beim Replizieren von Änderungen vom lokalen Speicher zum Server Zustandsbezeichner, die "UPLOAD" und Datenstrukturen mit dem Präfix "UP" angeben (z. **B. LR_SYNC_UPLOAD_HIERARCHY** und **[UPHIER).](uphier.md)** Verwenden Sie beim Replizieren von Änderungen vom Server zum lokalen Speicher Statusbezeichner, die "DOWNLOAD" und Datenstrukturen mit dem Präfix "DN" angeben (z. **B. LR_SYNC_DOWNLOAD_HIERARCHY** und **[DNHIER).](dnhier.md)** 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Replizierte Daten** <br/> |**Statusbezeichner** <br/> |**Datenstruktur** <br/> |
|[Zustand „Leerlauf“](idle-state.md) <br/> | *Keine*  <br/> |**LR_SYNC_IDLE** <br/> | *Keine*  <br/> |
|[Zustand „Synchronisieren“](synchronize-state.md) <br/> |Ordner oder Elemente  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Hochladen Hierarchiestatus](upload-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Hochladen Ordnerstatus](upload-folder-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |Elemente  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Hochladen Tabellenstatus](upload-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Hochladen Nachrichtenstatus](upload-message-state.md) <br/> |Element  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Hochladen Status des Lesestatus](upload-read-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[statusstatus Hochladen löschen](upload-delete-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Downloadhierarchiestatus](download-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Downloadtabellenstatus](download-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Status der Nachrichtenkopfzeile herunterladen](download-message-header-state.md) <br/> |Nachrichtenkopf  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Zustandsübergangsdiagramm

Das folgende Diagramm zeigt die Zustandsübergänge, die beim Hochladen oder Ausführen einer vollständigen Synchronisierung (downloading followed by uploading) von Ordnern oder Inhalten von Ordnern (E-Mail, Kalender, Kontakt, Notiz, Aufgabe oder Journalelemente) auftreten. 
  
@@@@@NEED, UM HIER FEHLENDE GRAFIK EINZUFÜGEN @@@@@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Beispiel: Hochladen einer Ordnerhierarchie

 Beim Hochladen einer Ordnerhierarchie werden die folgenden Schritte ausgeführt: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Schritt** <br/> |**Aktion** <br/> |**State** <br/> |**Verwandte Datenstruktur** <br/> |
|1.  <br/> |Der Client initiiert den Hierarchieupload mit **IOSTX::SyncBeg.**  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPHIER** mit Informationen für den Client. Dazu gehört die Initialisierung der [out]-Parameter:  *iEnt*  ist auf 0 festgelegt, und  *cEnt*  auf die Anzahl der Ordner in der Hierarchie, die hochgeladen werden müssen.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Der Client führt den tatsächlichen Hierarchieupload durch. Wenn  *cEnt*  beispielsweise 10 ist, ruft der Client für jeden der 10 Ordner **IOSTX::SyncBeg** auf und gibt den entsprechenden Statusbezeichner und die Datenstruktur für das Hochladen eines Ordners an.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPFLD** durch Initialisieren der [out]-Parameter auf, einschließlich des Grunds für den Ordnerupload, des Zeigers auf das Ordnerobjekt und der Eintrags-ID für den Ordner.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Der Client lädt den angegebenen Ordner hoch.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Ordneruploads: Bei Erfolg legt der Client den [in]-Parameter  *ulFlags*  in **UPFLD** mit **UPF_OK** fest und ruft dann **IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd** auf. Bei einem Fehler würde der Client  *"ulFlags"*  nicht mit dem **Flag "UPF_OK"** festlegen. **IOSTX::SetSyncResult** wird aufgerufen, wobei der **HRESULT-Wert** übergeben wird, und **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Wenn **UPF_OK** festgelegt ist, löscht Outlook 2013 oder Outlook 2010 die interne Anforderung zum Hochladen des Ordners. Unabhängig vom Status von  *ulFlags*  werden dann alle internen Buchführungsinformationen bereinigt. Während sich noch Ordner in der Hierarchie befinden, die hochgeladen werden müssen (*iEnt* ist immer noch kleiner als *cEnt*), wiederholen Sie die Schritte 3 bis 7 vom Client und Outlook 2013 oder Outlook 2010.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Hierarchieuploads: Bei Erfolg legt der Client das [in]-Flag in **UPHIER** mit **UPH_OK** fest und ruft dann **IOSTX::SetSyncResult (S_OK)** und **IOSTX::SyncEnd** auf. Bei einem Fehler würde der Client das **UPH_OK** Flag nicht festlegen. **IOSTX::SetSyncResult** wird aufgerufen, wobei der **HRESULT-Wert** übergeben wird, und **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Wenn **UPH_OK** festgelegt ist, löscht Outlook 2013 oder Outlook 2010 die interne Anforderung zum Hochladen der Hierarchie. Unabhängig vom Status von  *ulFlags*  werden dann alle internen Buchführungsinformationen bereinigt.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)


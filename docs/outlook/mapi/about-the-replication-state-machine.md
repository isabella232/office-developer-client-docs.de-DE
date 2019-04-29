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
  
Dieses Thema enthält eine Übersicht über den Statuscomputer für Microsoft Outlook 2013 und Microsoft Outlook 2010-Datenreplikation.
  
> [!NOTE]
> Die Replikations-API muss vollständig gemäß den Anweisungen in diesem Thema implementiert werden, damit Sie nützlich oder unterstützt werden. Die Replikations-API steht ausschließlich zum Replizieren von Outlook 2013-oder Outlook 2010-Änderungen auf und von einem Server zur Verfügung. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX und der Statuscomputer

Ein Client ruft **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, **[IOSTX:: SyncEnd](iostx-syncend.md)**, **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** und **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** in einer Sequenz auf, um Outlook 2013-oder Outlook 2010-Ordner und-Elemente zwischen einem lokalen Speicher und einem Server zu synchronisieren. Die tatsächliche Abfolge von Anrufen hängt von den zu replizierenden Daten ab (beispielsweise einer Hierarchie von Outlook 2013-oder Outlook 2010-Ordnern, einem Outlook 2013-oder Outlook 2010-Ordner, e-Mail-Elementen, Kalenderelementen usw.) und der Synchronisierungsrichtung (unabhängig davon, ob Hochladen vom lokalen Speicher zum Server oder Herunterladen vom Server zum lokalen Speicher). Es folgt eine typische Abfolge von anrufen: 
  
1. Der Client ruft **IOSTX:: SyncBeg** auf, um mit der Replikation zu beginnen und einen Statusbezeichner und einen Zeiger auf eine Adresse einer entsprechenden Datenstruktur anzugeben. 
    
2. Outlook 2013 oder Outlook 2010 weist die Datenstruktur zu und initialisiert die Datenstruktur mit den erforderlichen Informationen für den Client. 
    
3. Der Client führt die Replikation durch und aktualisiert die Datenstruktur, um alle erforderlichen Informationen zur Replikation an den lokalen Speicher zu übermitteln.
    
4. Nach der Durchführung der Replikation ruft der Client **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** und **IOSTX:: SyncEnd** auf, um den lokalen Speicher über den Abschluss der jeweiligen Replikation zu informieren. 
    
> [!NOTE]
> Der Client ruft immer **IOSTX:: SyncEnd** auf, um eine Replikation zu beenden, die der Client für einen bestimmten Status gestartet hat. Abhängig von den Gesamtdaten, die der Client synchronisieren muss, kann der Client das Paar von Aufrufen **IOSTX:: SyncBeg** und **IOSTX:: SyncEnd** mehrmals aufrufen. 
  
## <a name="state-table"></a>Statustabelle

> [!NOTE]
> In der folgenden Tabelle sind alle gültigen Status im Replikationsstatus Computer zusammen mit den entsprechenden Zustands-IDs und Datenstrukturen aufgeführt. In der Spalte **replizierte Daten** enthält der Begriff "Elemente" die Elemente e-Mail, Kalender, Kontakt, Notiz, Journal und Aufgaben. Beim Replizieren von Änderungen vom lokalen Speicher auf den Server verwenden Sie Statusbezeichner, die "UPLOAD" und Datenstrukturen mit dem Präfix "UP" angeben (beispielsweise **LR_SYNC_UPLOAD_HIERARCHY** und **[uphier](uphier.md)** ). Beim Replizieren von Änderungen vom Server zum lokalen Speicher verwenden Sie Statusbezeichner, die "DOWNLOAD" und Datenstrukturen mit dem Präfix "DN" angeben (beispielsweise **LR_SYNC_DOWNLOAD_HIERARCHY** und **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Replizierte Daten** <br/> |**Status-ID** <br/> |**Datenstruktur** <br/> |
|[Zustand „Leerlauf“](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Zustand „Synchronisieren“](synchronize-state.md) <br/> |Ordner oder Elemente  <br/> |**LR_SYNC** <br/> |**[SYNCHRONISIERUNGS](sync.md)** <br/> |
|[Hierarchie Status hochladen](upload-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Ordner Status hochladen](upload-folder-state.md) <br/> |Ordner  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Synchronisieren des Inhaltsstatus](synchronize-contents-state.md) <br/> |Elemente  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Tabellenstatus hochladen](upload-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Nachrichtenstatus hochladen](upload-message-state.md) <br/> |Element  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Status Status des Uploads](upload-read-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Status "Löschvorgang löschen"](upload-delete-status-state.md) <br/> |Elemente  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Download-Hierarchie Status](download-hierarchy-state.md) <br/> |Ordner  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Tabellenstatus herunterladen](download-table-state.md) <br/> |Elemente  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Nachrichtenkopf Status herunterladen](download-message-header-state.md) <br/> |Nachrichtenkopf  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>ZustandsÜbergang-Diagramm

Das folgende Diagramm zeigt die Zustandsübergänge, die beim Hochladen oder Ausführen einer vollständigen Synchronisierung (herunterladen gefolgt von einem Upload) von Ordnern oder Inhalten von Ordnern (e-Mail-, Kalender-, Kontakt-, Aufgaben-oder Journalelemente) auftreten. 
  
@ @ @ @ @NEED ZUM EINFÜGEN VON KUNST HIER, DIE @ @ @ @ @ @ FEHLT
  
## <a name="example-uploading-a-folder-hierarchy"></a>Beispiel: Hochladen einer Ordnerhierarchie

 Beim Hochladen einer Ordnerhierarchie erfolgen die folgenden Schritte: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Schritt** <br/> |**Aktion** <br/> |**State** <br/> |**Zugehörige Datenstruktur** <br/> |
|1.  <br/> |Der Client initiiert den Hierarchie Upload mit **IOSTX:: SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 oder Outlook 2010 füllt **uphier** mit Informationen für den Client. Dazu gehört das Initialisieren der [out]-Parameter: *iEnt* ist auf 0 und *cEnt* auf die Anzahl der Ordner in der Hierarchie festgelegt, die hochgeladen werden müssen.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |Der Client führt den tatsächlichen Hierarchie Upload aus. Wenn *cEnt* beispielsweise 10 ist, ruft der Client für jeden der 10 Ordner **IOSTX:: SyncBeg**auf und gibt den entsprechenden Statusbezeichner und die Datenstruktur für das Hochladen eines Ordners an.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 oder Outlook 2010 füllt **UPFLD** durch Initialisieren der [out]-Parameter, einschließlich des Grunds für den Ordner Upload, des Zeigers auf das Folder-Objekt und der EINTRAGS-ID für den Ordner.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |Der Client lädt den angegebenen Ordner hoch.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Ordner Uploads: bei Erfolg legt der Client den [in]-Parameter *ulFlags* in **UPFLD** mit **UPF_OK**fest und ruft dann **IOSTX:: SetSyncResult (S_OK)** und **IOSTX:: SyncEnd **. Bei einem fehlschlagen würde der Client *ulFlags* nicht mit dem **UPF_OK** -Flag festlegen. Sie ruft **IOSTX:: SetSyncResult**auf und übergibt den **HRESULT** -Wert und **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Wenn **UPF_OK** festgelegt ist, wird die interne Anforderung für das Hochladen des Ordners von Outlook 2013 oder Outlook 2010 gelöscht. Unabhängig vom Status von *ulFlags* werden alle internen Buchhaltungsinformationen bereinigt. Während in der Hierarchie noch Ordner zum Hochladen vorhanden sind (*iEnt* ist immer noch kleiner als *cEnt*), wiederholen der Client und outlook 2013 oder Outlook 2010 die Schritte 3 bis 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |Der Client benachrichtigt den lokalen Speicher über den Abschluss des Hierarchie-Uploads: beim Erfolg legt der Client das [in]-Flag **** in uphier mit **UPH_OK**und dann **IOSTX:: SetSyncResult (S_OK)** und **IOSTX:: SyncEnd**. Bei einem fehlschlagen würde der Client das **UPH_OK** -Flag nicht festlegen. Sie ruft **IOSTX:: SetSyncResult**auf und übergibt den **HRESULT** -Wert und **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Wenn **UPH_OK** festgelegt ist, wird die interne Anforderung zum Hochladen der Hierarchie von Outlook 2013 oder Outlook 2010 gelöscht. Unabhängig vom Status von *ulFlags* werden alle internen Buchhaltungsinformationen bereinigt.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)


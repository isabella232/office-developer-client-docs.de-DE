---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 93fb82c6274a1703376d7a9e15f37088e132dc23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585892"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Stellt die Suchkriterien für den Container her.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert. Wenn NULL in der _LpRestriction_ -Parameter übergeben wird, werden die Suchkriterien, die für diesen Container zuletzt verwendet wurden erneut verwendet. NULL darf nicht in _LpRestriction_ für die erste Suche in einem Container übergeben werden. 
    
 _lpContainerList_
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichner, die Container, in die Suche einbezogen werden darstellen. Wenn ein Client NULL im Parameter _LpContainerList_ übergibt, werden die zuletzt verwendet, um diesen Container suchen Eintragsbezeichner für die neue Suche verwendet. Ein Client sollte nicht NULL _LpContainerList_ für die erste Suche in einem Container übergeben. 
    
 _ulSearchFlags_
  
> [in] Eine Bitmaske aus Flags, die steuern, wie die Suche ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
BACKGROUND_SEARCH 
  
> Die Suche sollte mit normaler Priorität relativ zu anderen Suchvorgänge ausgeführt. Dieses Kennzeichen können nicht gleichzeitig als das Flag FOREGROUND_SEARCH festgelegt werden.
    
FOREGROUND_SEARCH 
  
> Die Suche sollte mit hoher Priorität relativ zu anderen Suchvorgänge ausgeführt. Dieses Kennzeichen können nicht gleichzeitig als das Flag BACKGROUND_SEARCH festgelegt werden.
    
NON_CONTENT_INDEXED_SEARCH
  
> Die Suche sollte Inhaltsindex nicht übereinstimmenden Einträge suchen verwenden. Dieses Kennzeichen gilt nur für Exchange-Speicher.
    
RECURSIVE_SEARCH 
  
> Die Suche sollte in der _LpContainerList_ -Parameter und alle untergeordneten Container angegebenen Container enthalten. Dieses Kennzeichen können nicht gleichzeitig als das Flag SHALLOW_SEARCH festgelegt werden. 
    
RESTART_SEARCH 
  
> Die Suche sollte initiiert, wenn dies der erste Aufruf von **SetSearchCriteria**ist, oder neu gestartet, wenn die Suche nicht aktiv ist. Dieses Kennzeichen können nicht gleichzeitig als das Flag STOP_SEARCH festgelegt werden.
    
SHALLOW_SEARCH 
  
> Die Suche sollte nur in den Containern im für übereinstimmende Einträge _LpContainerList_ -Parameter angegebene aussehen. Dieses Kennzeichen können nicht gleichzeitig als das Flag RECURSIVE_SEARCH festgelegt werden. 
    
STOP_SEARCH 
  
> Die Suche muss angehalten werden. Dieses Kennzeichen können nicht gleichzeitig als das Flag RESTART_SEARCH festgelegt werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Suchkriterien wurde erfolgreich festgelegt.
    
MAPI_E_TOO_COMPLEX 
  
> Der Dienstanbieter unterstützt nicht die angegebenen Suchkriterien entsprechen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIContainer::SetSearchCriteria** -Methode richtet Suchkriterien für einen Container, der sucht, in der Regel in einem Suchergebnisse Ordner unterstützt. Suchergebnisse Ordner enthält Links zu Nachrichten, die den Suchkriterien entsprechen; die Nachrichten werden weiterhin an ihrem ursprünglichen Speicherort gespeichert. Nur eindeutigen in einem Suchergebnisse Ordner enthaltenen Daten ist die Inhaltstabelle. Die Inhaltstabelle eines Ordners Suchergebnisse hat den zusammengeführten Inhalt des Nachrichtenspeichers, nachdem die Suche Einschränkung angewendet wurde. 
  
Suchvorgang funktioniert nur für diese Tabelle zusammengeführten Inhalt. Es wird nicht durch andere Suchergebnisse Ordner gesucht. Die Suchergebnisse zurück, nur die Nachrichten, die den Suchkriterien entsprechen. Die Ordnerhierarchie wird nicht zurückgegeben.
  
Steuerelement wird an den Client zurückgegeben, wenn die Suche abgeschlossen wurde.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Address Book Containern erstellen Suchkriterien Einschränkungen auf ihren Inhalt Tabellen anwenden. Weitere Informationen zu Suchkriterien und address Book Containern, finden Sie unter [Implementieren erweiterte Suche](implementing-advanced-searching.md).
  
Sie sollten unterstützen öffnen, kopieren, verschieben und delete-Vorgänge auf die Nachrichten in Suchergebnissen Ordnern, nicht auf den Suchergebnisse Ordner selbst. Lassen Sie nicht Nachrichten innerhalb erstellt oder in einem Suchergebnisse Ordner kopiert werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie zum Suchen der Empfänger der Nachricht _LpRestriction_ So zeigen Sie auf eine Einschränkung Unterobjekts mit dem **UlSubObject** -Element in der [SSubRestriction](ssubrestriction.md) -Struktur auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) festgelegt. Legen Sie zum Suchen nach Anlagen des **UlSubObject** Members auf **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Legen Sie den **LpRes** Member So zeigen Sie auf eine eigenschaftseinschränkung, die die Suchkriterien für die Empfänger oder Anlagen beschreibt. 
  
Um für Dateianlagen zu suchen, die die Erweiterung .mss haben, legen Sie beispielsweise **UlSubObject** auf **PR_MESSAGE_ATTACHMENTS** und **LpRes** , die eine eigenschaftseinschränkung, die mit **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) übereinstimmt ) mit. mss.
  
Festlegen des Flags FOREGROUND_SEARCH in der _UlSearchFlags_ -Parameter kann eine Beeinträchtigung der Systemleistung führen. 
  
**SetSearchCriteria** können Sie die Suchkriterien bereits in Bearbeitung einer Suche ändern. Sie können neue Einschränkungen, neue Listen der Ordner für die Suche und eine neue Suche Priorität wie aktualisieren eine Suche auf eine höhere Priorität angeben. Änderungen in Search Priorität bewirken keine vorhandene Suche neu starten, jedoch können weitere Änderungen an den Suchkriterien. 
  
Wenn Sie über die Verwendung eines Ordners-Ergebnisse sind, können Sie den Ordner löschen oder lassen Sie ihn zur späteren Verwendung geöffnet bleiben. Wenn Sie den Suchergebnisse Ordner löschen, werden nur Nachricht Links gelöscht. Die tatsächlichen Nachrichten verbleiben in die übergeordneten Ordner. 
  
Weitere Informationen zu Suchergebnissen Ordnern finden Sie unter [Suchordner MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI (engl.) verwendet die **IMAPIContainer::SetSearchCriteria** -Methode zum Schreiben von Suchkriterien für einen Ordner, nachdem ein Benutzer es bearbeitet wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


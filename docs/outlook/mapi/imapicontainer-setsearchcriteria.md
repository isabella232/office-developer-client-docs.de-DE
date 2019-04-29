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
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427199"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt Suchkriterien für den Container fest.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> in Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert. Wenn NULL im _lpRestriction_ -Parameter übergeben wird, werden die Suchkriterien, die zuletzt für diesen Container verwendet wurden, erneut verwendet. NULL sollte in _lpRestriction_ nicht für die erste Suche in einem Container übergeben werden. 
    
 _lpContainerList_
  
> in Ein Zeiger auf ein Array von Eintrags Bezeichnern, die Container darstellen, die in die Suche eingeschlossen werden sollen. Wenn ein Client im _lpContainerList_ -Parameter den Wert NULL übergibt, werden die in letzter Zeit verwendeten Eintrags-IDs für die neue Suche verwendet. Ein Client sollte NULL in _lpContainerList_ für die erste Suche in einem Container nicht weiterleiten. 
    
 _ulSearchFlags_
  
> in Eine Bitmaske von Flags, die Steuern, wie die Suche ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
BACKGROUND_SEARCH 
  
> Die Suche sollte im Verhältnis zu anderen Suchvorgängen mit normaler Priorität ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem FOREGROUND_SEARCH-Flag festgelegt werden.
    
FOREGROUND_SEARCH 
  
> Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem BACKGROUND_SEARCH-Flag festgelegt werden.
    
NON_CONTENT_INDEXED_SEARCH
  
> Die Suche sollte nicht die Inhaltsindizierung verwenden, um übereinstimmende Einträge zu finden. Dieses Flag gilt nur für Exchange-Speicher.
    
RECURSIVE_SEARCH 
  
> Die Suche muss die im Parameter _lpContainerList_ und alle untergeordneten Container angegebenen Container aufweisen. Dieses Flag kann nicht gleichzeitig mit dem SHALLOW_SEARCH-Flag festgelegt werden. 
    
RESTART_SEARCH 
  
> Die Suche sollte initiiert werden, wenn dies der erste Aufruf von **SetSearchCriteria**ist, oder neu gestartet, wenn die Suche inaktiv ist. Dieses Flag kann nicht gleichzeitig mit dem STOP_SEARCH-Flag festgelegt werden.
    
SHALLOW_SEARCH 
  
> Die Suche sollte nur in den im _lpContainerList_ -Parameter angegebenen Containern für übereinstimmende Einträge aussehen. Dieses Flag kann nicht gleichzeitig mit dem RECURSIVE_SEARCH-Flag festgelegt werden. 
    
STOP_SEARCH 
  
> Die Suche sollte beendet werden. Dieses Flag kann nicht gleichzeitig mit dem RESTART_SEARCH-Flag festgelegt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich festgelegt.
    
MAPI_E_TOO_COMPLEX 
  
> Der Dienstanbieter unterstützt die angegebenen Suchkriterien nicht.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMAPIContainer:: SetSearchCriteria** -Methode werden Suchkriterien für einen Container festgelegt, der Suchvorgänge unterstützt, in der Regel ein Suchergebnisordner. Ein Suchergebnisordner enthält Links zu den Nachrichten, die den Suchkriterien entsprechen. die tatsächlichen Nachrichten werden weiterhin an ihren ursprünglichen Speicherorten gespeichert. Die einzigen eindeutigen Daten, die in einem Ordner mit Suchergebnissen enthalten sind, sind die Inhaltstabelle. Die Inhaltstabelle eines Suchergebnis Ordners enthält die zusammengeführten Inhalte des Nachrichtenspeichers, nachdem die sucheinschränkung angewendet wurde. 
  
Ein Suchvorgang funktioniert nur in dieser zusammengeführten Inhaltstabelle; andere Suchergebnisordner werden nicht durchsucht. In den Suchergebnissen werden nur die Nachrichten zurückgegeben, die den Suchkriterien entsprechen. die Ordnerhierarchie wird nicht zurückgegeben.
  
Die Steuerung wird an den Client zurückgegeben, wenn die Suche abgeschlossen ist.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer legen Suchkriterien fest, indem Sie Einschränkungen auf Ihre Inhaltstabellen anwenden. Weitere Informationen zu Suchkriterien und Adressbuch Containern finden Sie unter [Implementieren der erweiterten Suche](implementing-advanced-searching.md).
  
Sie sollten öffnen-, Kopier-, Verschiebungs-und Löschvorgänge für die Nachrichten in Suchergebnis Ordnern unterstützen, nicht im Ordner "Suchergebnisse" selbst. Lassen Sie keine Nachrichten innerhalb oder in einen Suchergebnisordner kopieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Suchen nach Nachrichtenempfängern legen Sie fest, dass _lpRestriction_ auf eine SubObject-Einschränkung zeigt, wobei das **ulSubObject** -Element in der [SSubRestriction](ssubrestriction.md) -Struktur auf **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) festgelegt ist. Legen Sie das **ulSubObject** -Element auf **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md)) fest, um nach Anlagen zu suchen. Legen Sie fest, dass das **lpRes** -Element auf eine Eigenschaftseinschränkung zeigt, die die Suchkriterien für die Empfänger oder Anlagen beschreibt. 
  
Um beispielsweise nach Dateianlagen mit der Erweiterung. MSS zu suchen, legen Sie **ulSubObject** auf **PR_MESSAGE_ATTACHMENTS** und **lpRes** auf eine Eigenschaftseinschränkung fest, die mit **PR_ATTACH_EXTENSION** übereinstimmt ([pidtagattachextension (](pidtagattachextension-canonical-property.md) ) mit. MSS.
  
Das Festlegen des FOREGROUND_SEARCH-Flags im _ulSearchFlags_ -Parameter kann zu einer Verringerung der Systemleistung führen. 
  
Sie können **SetSearchCriteria** verwenden, um die Suchkriterien einer bereits ausgeführten Suche zu ändern. Sie können neue Einschränkungen, neue Ordnerlisten für die Suche und eine neue Suchpriorität angeben, wie beispielsweise das Upgrade einer Suche auf eine höhere Priorität. Änderungen der Suchpriorität führen nicht zu einem Neustart einer vorhandenen Suche, andere Änderungen an den Suchkriterien können jedoch vorgenommen werden. 
  
Wenn Sie einen Suchergebnisordner verwenden, können Sie entweder den Ordner löschen oder ihn zur späteren Verwendung geöffnet lassen. Wenn Sie den Ordner Suchergebnisse löschen, werden nur die Nachrichten Links gelöscht. Die tatsächlichen Nachrichten verbleiben in ihren übergeordneten Ordnern. 
  
Weitere Informationen zu Suchergebnis Ordnern finden Sie unter [MAPI Search Folders](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI verwendet die **IMAPIContainer:: SetSearchCriteria** -Methode, um Suchkriterien für einen Ordner zu schreiben, nachdem Sie von einem Benutzer bearbeitet wurde.  <br/> |
   
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


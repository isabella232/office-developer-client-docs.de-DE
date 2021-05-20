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
  
> [in] Ein Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien definiert. Wenn NULL im  _lpRestriction-Parameter_ übergeben wird, werden die Suchkriterien, die zuletzt für diesen Container verwendet wurden, erneut verwendet. NULL sollte nicht in  _lpRestriction_ für die erste Suche in einem Container übergeben werden. 
    
 _lpContainerList_
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichnern, die Container darstellen, die in die Suche einbezogen werden sollen. Wenn ein Client NULL im  _lpContainerList-Parameter übergibt,_ werden die eintragsbezeichner, die zuletzt zum Durchsuchen dieses Containers verwendet wurden, für die neue Suche verwendet. Ein Client sollte null nicht in  _lpContainerList_ für die erste Suche in einem Container übergeben. 
    
 _ulSearchFlags_
  
> [in] Eine Bitmaske mit Flags, die steuern, wie die Suche ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
BACKGROUND_SEARCH 
  
> Die Suche sollte mit normaler Priorität im Verhältnis zu anderen Suchen ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem FOREGROUND_SEARCH festgelegt werden.
    
FOREGROUND_SEARCH 
  
> Die Suche sollte mit hoher Priorität im Vergleich zu anderen Suchen ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem BACKGROUND_SEARCH festgelegt werden.
    
NON_CONTENT_INDEXED_SEARCH
  
> Die Suche sollte keine Inhaltsindizierung verwenden, um übereinstimmende Einträge zu finden. Dieses Flag ist nur für Exchange gültig.
    
RECURSIVE_SEARCH 
  
> Die Suche sollte die im  _lpContainerList-Parameter_ angegebenen Container und alle untergeordneten Container enthalten. Dieses Flag kann nicht gleichzeitig mit dem SHALLOW_SEARCH festgelegt werden. 
    
RESTART_SEARCH 
  
> Die Suche sollte initiiert werden, wenn dies der erste Aufruf von **SetSearchCriteria** ist, oder neu gestartet werden, wenn die Suche inaktiv ist. Dieses Flag kann nicht gleichzeitig mit dem STOP_SEARCH festgelegt werden.
    
SHALLOW_SEARCH 
  
> Die Suche sollte nur in den im  _lpContainerList-Parameter_ angegebenen Containern nach übereinstimmenden Einträgen suchen. Dieses Flag kann nicht gleichzeitig mit dem RECURSIVE_SEARCH festgelegt werden. 
    
STOP_SEARCH 
  
> Die Suche sollte beendet werden. Dieses Flag kann nicht gleichzeitig mit dem RESTART_SEARCH festgelegt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich festgelegt.
    
MAPI_E_TOO_COMPLEX 
  
> Der Dienstanbieter unterstützt die angegebenen Suchkriterien nicht.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::SetSearchCriteria-Methode** richtet Suchkriterien für einen Container ein, der Suchen unterstützt, in der Regel ein Suchergebnisordner. Ein Suchergebnisordner enthält Links zu den Nachrichten, die den Suchkriterien entsprechen. die tatsächlichen Nachrichten werden weiterhin an ihren ursprünglichen Speicherorten gespeichert. Die einzigen eindeutigen Daten, die in einem Suchergebnisordner enthalten sind, ist die Inhaltstabelle. Das Inhaltsverzeichnis eines Suchergebnisordners enthält den zusammengeführten Inhalt des Nachrichtenspeichers, nachdem die Sucheinschränkung angewendet wurde. 
  
Ein Suchvorgang funktioniert nur für diese zusammengeführte Inhaltstabelle. Andere Suchergebnisse werden nicht durchsucht. Die Suchergebnisse geben nur die Nachrichten zurück, die den Suchkriterien entsprechen. Die Ordnerhierarchie wird nicht zurückgegeben.
  
Das Steuerelement wird an den Client zurückgegeben, wenn die Suche abgeschlossen ist.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer richten Suchkriterien durch Anwenden von Einschränkungen auf ihre Inhaltstabellen ein. Weitere Informationen zu Suchkriterien und Adressbuchcontainern finden Sie unter [Implementing Advanced Searching](implementing-advanced-searching.md).
  
Sie sollten Vorgänge zum Öffnen, Kopieren, Verschieben und Löschen von Nachrichten in Suchergebnissen und nicht im Suchergebnisordner selbst unterstützen. Lassen Sie nicht zu, dass Nachrichten innerhalb eines Suchergebnisordners erstellt oder in diesen kopiert werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie zum Suchen nach Nachrichtenempfängern fest, dass  _lpRestriction_ auf eine Unterobjekteinschränkung mit dem **ulSubObject-Element** in der [SSubRestriction-Struktur](ssubrestriction.md) auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) verweisen soll. Um nach Anlagen zu suchen, legen Sie das **element ulSubObject** auf **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fest. Legen Sie **das lpRes-Element** so fest, dass es auf eine Eigenschaftseinschränkung zeigt, die die Suchkriterien für die Empfänger oder Anlagen beschreibt. 
  
Wenn Sie beispielsweise nach Dateianlagen suchen möchten, die die Erweiterung .mss haben, legen Sie **ulSubObject** auf **PR_MESSAGE_ATTACHMENTS** und **lpRes** auf eine Eigenschaftseinschränkung fest, die PR_ATTACH_EXTENSION ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) mit **.mss** entspricht.
  
Wenn Sie FOREGROUND_SEARCH im  _ulSearchFlags-Parameter_ festlegen, kann die Systemleistung sinken. 
  
Sie können **SetSearchCriteria verwenden,** um die Suchkriterien einer bereits ausgeführten Suche zu ändern. Sie können neue Einschränkungen, neue Listen von zu durchsuchenden Ordnern und eine neue Suchpriorität angeben, z. B. das Upgrade einer Suche auf eine höhere Priorität. Änderungen an der Suchpriorität führen nicht dazu, dass eine vorhandene Suche neu gestartet wird, aber andere Änderungen an Suchkriterien können dazu führen. 
  
Wenn Sie einen Suchergebnisordner verwenden, können Sie den Ordner entweder löschen oder für eine spätere Verwendung geöffnet lassen. Wenn Sie den Suchergebnisordner löschen, werden nur Nachrichtenlinks gelöscht. Die tatsächlichen Nachrichten verbleiben in ihren übergeordneten Ordnern. 
  
Weitere Informationen zu Suchergebnissen finden Sie unter [MAPI Search Folders](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI verwendet die **IMAPIContainer::SetSearchCriteria-Methode,** um Suchkriterien für einen Ordner zu schreiben, nachdem ein Benutzer ihn bearbeitet hat.  <br/> |
   
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


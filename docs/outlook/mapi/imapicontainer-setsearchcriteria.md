---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d980b6a1c45bfae23e1ad48b2bc139ec98f7efe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576072"
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
  
> [in] Ein Zeiger auf ein Array von Eintragsbezeichnern, die Container darstellen, die in die Suche einbezogen werden sollen. Wenn ein Client NULL im  _lpContainerList-Parameter_ übergibt, werden die Eintragsbezeichner, die zuletzt zum Durchsuchen dieses Containers verwendet wurden, für die neue Suche verwendet. Ein Client sollte null in  _lpContainerList_ für die erste Suche in einem Container nicht übergeben. 
    
 _ulSearchFlags_
  
> [in] Eine Bitmaske mit Flags, die steuern, wie die Suche ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
BACKGROUND_SEARCH 
  
> Die Suche sollte relativ zu anderen Suchvorgängen mit normaler Priorität ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem FOREGROUND_SEARCH-Flag festgelegt werden.
    
FOREGROUND_SEARCH 
  
> Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden. Dieses Flag kann nicht gleichzeitig mit dem BACKGROUND_SEARCH-Flag festgelegt werden.
    
NON_CONTENT_INDEXED_SEARCH
  
> Die Suche sollte keine Inhaltsindizierung verwenden, um übereinstimmende Einträge zu finden. Dieses Kennzeichen gilt nur für Exchange Speicher.
    
RECURSIVE_SEARCH 
  
> Die Suche sollte die im  _lpContainerList-Parameter_ angegebenen Container und alle untergeordneten Container enthalten. Dieses Flag kann nicht gleichzeitig mit dem SHALLOW_SEARCH-Flag festgelegt werden. 
    
RESTART_SEARCH 
  
> Die Suche sollte initiiert werden, wenn dies der erste Aufruf von **SetSearchCriteria** ist, oder neu gestartet werden, wenn die Suche inaktiv ist. Dieses Flag kann nicht gleichzeitig mit dem STOP_SEARCH-Flag festgelegt werden.
    
SHALLOW_SEARCH 
  
> Die Suche sollte nur in den im  _lpContainerList-Parameter_ angegebenen Containern nach übereinstimmenden Einträgen suchen. Dieses Flag kann nicht gleichzeitig mit dem RECURSIVE_SEARCH-Flag festgelegt werden. 
    
STOP_SEARCH 
  
> Die Suche sollte beendet werden. Dieses Flag kann nicht gleichzeitig mit dem RESTART_SEARCH-Flag festgelegt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich festgelegt.
    
MAPI_E_TOO_COMPLEX 
  
> Der Dienstanbieter unterstützt die angegebenen Suchkriterien nicht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIContainer::SetSearchCriteria-Methode** richtet Suchkriterien für einen Container ein, der Suchvorgänge unterstützt, in der Regel einen Suchergebnisordner. Ein Suchergebnisordner enthält Links zu den Nachrichten, die die Suchkriterien erfüllen. Die tatsächlichen Nachrichten werden weiterhin an ihren ursprünglichen Speicherorten gespeichert. Die einzigen eindeutigen Daten, die in einem Suchergebnisordner enthalten sind, sind das Inhaltsverzeichnis. Das Inhaltsverzeichnis eines Suchergebnisordners enthält die zusammengeführten Inhalte des Nachrichtenspeichers, nachdem die Sucheinschränkung angewendet wurde. 
  
Ein Suchvorgang funktioniert nur in diesem zusammengeführten Inhaltsverzeichnis. Es werden keine anderen Suchergebnisordner durchsucht. Die Suchergebnisse geben nur die Nachrichten zurück, die den Suchkriterien entsprechen. die Ordnerhierarchie wird nicht zurückgegeben.
  
Die Steuerung wird an den Client zurückgegeben, wenn die Suche abgeschlossen ist.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer legen Suchkriterien fest, indem sie Einschränkungen auf ihre Inhaltsverzeichnisse anwenden. Weitere Informationen zu Suchkriterien und Adressbuchcontainern finden Sie unter [Implementieren der erweiterten Suche.](implementing-advanced-searching.md)
  
Sie sollten Vorgänge zum Öffnen, Kopieren, Verschieben und Löschen von Nachrichten in Suchergebnisordnern unterstützen, nicht für den Suchergebnisordner selbst. Lassen Sie nicht zu, dass Nachrichten in einem Suchergebnisordner erstellt oder in diesen kopiert werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um nach Nachrichtenempfängern zu suchen, legen Sie  _lpRestriction_ so fest, dass sie auf eine Unterobjekteinschränkung verweist, wobei das **UlSubObject-Element** in der [SSubRestriction-Struktur](ssubrestriction.md) auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) festgelegt ist. Um nach Anlagen zu suchen, legen Sie das **UlSubObject-Element** auf **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) fest. Legen Sie das **lpRes-Element** so fest, dass es auf eine Eigenschaftseinschränkung zeigt, die die Suchkriterien für die Empfänger oder Anlagen beschreibt. 
  
Wenn Sie z. B. nach Dateianlagen mit der Erweiterung MSS suchen möchten, legen Sie **"ulSubObject"** auf **PR_MESSAGE_ATTACHMENTS** und **"lpRes"** auf eine Eigenschaftseinschränkung fest, die **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) mit MSS übereinstimmt.
  
Das Festlegen des FOREGROUND_SEARCH Flags im  _ulSearchFlags-Parameter_ kann zu einer Beeinträchtigung der Systemleistung führen. 
  
Sie können **SetSearchCriteria** verwenden, um die Suchkriterien einer bereits ausgeführten Suche zu ändern. Sie können neue Einschränkungen, neue Listen mit zu durchsuchenden Ordnern und eine neue Suchpriorität angeben, z. B. ein Upgrade einer Suche auf eine höhere Priorität. Änderungen an der Suchpriorität führen nicht dazu, dass eine vorhandene Suche neu gestartet wird, aber andere Änderungen an den Suchkriterien sind möglich. 
  
Wenn Sie einen Suchergebnisordner verwenden, können Sie den Ordner löschen oder ihn zur späteren Verwendung geöffnet lassen. Wenn Sie den Suchergebnisordner löschen, werden nur Nachrichtenlinks gelöscht. Die tatsächlichen Nachrichten verbleiben in ihren übergeordneten Ordnern. 
  
Weitere Informationen zu Suchergebnisordnern finden Sie unter [MAPI-Suchordner.](mapi-search-folders.md) 
  
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


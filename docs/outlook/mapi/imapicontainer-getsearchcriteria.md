---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412023"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die Suchkriterien für den Container ab.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lppRestriction_
  
> Out Ein Zeiger auf einen Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert. Wenn eine Clientanwendung im _lppRestriction_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** keine **SRestriction** -Struktur zurück. 
    
 _lppContainerList_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Eintrags Bezeichnern, die Container darstellen, die in die Suche eingeschlossen werden sollen. Wenn ein Client im _lppContainerList_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** kein Array von Eintrags Bezeichnern zurück. 
    
 _lpulSearchState_
  
> Out Ein Zeiger auf eine Bitmaske von Flags, die verwendet werden, um den aktuellen Status der Suche anzugeben. Wenn ein Client im _lpulSearchState_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** keine Flags zurück. Die folgenden Flags können festgelegt werden: 
    
SEARCH_FOREGROUND 
  
> Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden. Wenn dieses Flag nicht festgelegt ist, wird die Suche im Verhältnis zu anderen Suchvorgängen mit normaler Priorität ausgeführt.
    
SEARCH_REBUILD 
  
> Die Suche befindet sich im CPU-intensiven Modus des Vorgangs und versucht, Nachrichten zu finden, die den Kriterien entsprechen. Wenn dieses Flag nicht festgelegt ist, ist der CPU-intensive Teil des Suchvorgangs über. Dieses Flag hat nur dann eine Bedeutung, wenn die Suche aktiv ist (d. h., wenn das SEARCH_RUNNING-Flag festgelegt ist).
    
SEARCH_RECURSIVE 
  
> Die Suche sucht in den angegebenen Containern und allen untergeordneten Containern nach übereinstimmenden Einträgen. Wenn dieses Flag nicht festgelegt ist, werden nur die Container durchsucht, die explizit im letzten Aufruf der [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode enthalten sind. 
    
SEARCH_RUNNING 
  
> Die Suche ist aktiv, und die Inhaltstabelle des Containers wird aktualisiert, um Änderungen im Nachrichtenspeicher oder im Adressbuch widerzuspiegeln. Wenn dieses Flag nicht festgelegt ist, ist die Suche inaktiv und die Tabelle Contents ist statisch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Suchkriterien wurden nie für den Container festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer:: GetSearchCriteria** -Methode ruft die Suchkriterien für einen Container ab, der Suchvorgänge unterstützt, in der Regel einen Suchergebnisordner. Sie erstellen Suchkriterien, indem Sie die **IMAPIContainer:: SetSearchCriteria** -Methode eines Containers aufrufen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer müssen **GetSearchCriteria** möglicherweise nur unterstützen, wenn Sie die erweiterten Suchfunktionen zur Verfügung stellen, die der **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md))-Eigenschaft zugeordnet sind. Weitere Informationen dazu, wie Sie die erweiterte Suchfunktion für Adressbuchcontainer implementieren, finden Sie unter [Implementieren der erweiterten](implementing-advanced-searching.md)Suche.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie die Datenstrukturen, auf die durch die Parameter _lppRestriction_ und _lppContainerList_ verwiesen wird, nicht mehr aufgerufen haben, rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) einmal für jede Struktur auf, die freigegeben werden soll. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI verwendet die **IMAPIContainer:: GetSearchCriteria** -Methode, um Suchkriterien aus einem anzuzeigenden Ordner abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische Pidtagsearch (-Eigenschaft](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


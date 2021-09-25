---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 341ed6c416c3029b0e4498cd7c6009e246b23bae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596365"
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
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 _lppRestriction_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien definiert. Wenn eine Clientanwendung NULL im  _lppRestriction-Parameter_ übergibt, gibt **GetSearchCriteria** keine **SRestriction-Struktur** zurück. 
    
 _lppContainerList_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eintragsbezeichnern, die Container darstellen, die in die Suche einbezogen werden sollen. Wenn ein Client NULL im  _lppContainerList-Parameter_ übergibt, gibt **GetSearchCriteria** kein Array von Eintragsbezeichnern zurück. 
    
 _lpulSearchState_
  
> [out] Ein Zeiger auf eine Bitmaske mit Flags, die verwendet werden, um den aktuellen Status der Suche anzugeben. Wenn ein Client NULL im  _Parameter lpulSearchState_ übergibt, gibt **GetSearchCriteria** keine Flags zurück. Die folgenden Flags können festgelegt werden: 
    
SEARCH_FOREGROUND 
  
> Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden. Wenn dieses Kennzeichen nicht festgelegt ist, wird die Suche relativ zu anderen Suchvorgängen mit normaler Priorität ausgeführt.
    
SEARCH_REBUILD 
  
> Die Suche befindet sich im CPU-intensiven Modus des Vorgangs und versucht, Nachrichten zu suchen, die den Kriterien entsprechen. Wenn dieses Flag nicht festgelegt ist, ist der CPU-intensive Teil des Suchvorgangs beendet. Dieses Flag hat nur Dann Bedeutung, wenn die Suche aktiv ist (d. h. wenn das SEARCH_RUNNING-Flag festgelegt ist).
    
SEARCH_RECURSIVE 
  
> Die Suche sucht in angegebenen Containern und allen untergeordneten Containern nach übereinstimmenden Einträgen. Wenn dieses Flag nicht festgelegt ist, werden nur die Container durchsucht, die explizit im letzten Aufruf der [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) enthalten sind. 
    
SEARCH_RUNNING 
  
> Die Suche ist aktiv, und das Inhaltsverzeichnis des Containers wird aktualisiert, um Änderungen im Nachrichtenspeicher oder Adressbuch widerzuspiegeln. Wenn dieses Kennzeichen nicht festgelegt ist, ist die Suche inaktiv, und das Inhaltsverzeichnis ist statisch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Suchkriterien wurden für den Container nie festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIContainer::GetSearchCriteria-Methode** ruft die Suchkriterien für einen Container ab, der Suchvorgänge unterstützt, in der Regel einen Suchergebnisordner. Sie erstellen Suchkriterien, indem Sie die **IMAPIContainer::SetSearchCriteria-Methode** eines Containers aufrufen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer müssen **GetSearchCriteria** möglicherweise nur unterstützen, wenn sie die erweiterten Suchfunktionen bereitstellen, die der **eigenschaft PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) zugeordnet sind. Weitere Informationen zum Implementieren der erweiterten Suchfunktion für Adressbuchcontainer finden Sie unter [Implementieren der erweiterten Suche.](implementing-advanced-searching.md)
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie mit den Datenstrukturen fertig sind, auf die durch die Parameter  _"lppRestriction"_ und  _"lppContainerList"_ verwiesen wird, rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) einmal für jede zu freigebende Struktur auf. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI verwendet die **IMAPIContainer::GetSearchCriteria-Methode,** um Suchkriterien aus einem anzuzeigenden Ordner abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagSearch-Eigenschaft](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


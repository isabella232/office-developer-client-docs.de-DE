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
  
> [in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lppRestriction_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien definiert. Wenn eine Clientanwendung NULL im  _lppRestriction-Parameter_ übergibt, gibt **GetSearchCriteria** keine **SRestriction-Struktur** zurück. 
    
 _lppContainerList_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eintragsbezeichnern, die Container darstellen, die in die Suche einbezogen werden sollen. Wenn ein Client NULL im  _lppContainerList-Parameter übergibt,_ gibt **GetSearchCriteria** kein Array von Eintragsbezeichnern zurück. 
    
 _lpulSearchState_
  
> [out] Ein Zeiger auf eine Bitmaske mit Flags, die verwendet werden, um den aktuellen Status der Suche anzugeben. Wenn ein Client NULL im  _lpulSearchState-Parameter_ übergibt, gibt **GetSearchCriteria** keine Flags zurück. Die folgenden Kennzeichen können festgelegt werden: 
    
SEARCH_FOREGROUND 
  
> Die Suche sollte mit hoher Priorität im Vergleich zu anderen Suchen ausgeführt werden. Wenn dieses Flag nicht festgelegt ist, wird die Suche mit normaler Priorität im Verhältnis zu anderen Suchen ausgeführt.
    
SEARCH_REBUILD 
  
> Die Suche befindet sich im CPU-intensiven Modus des Vorgangs und versucht, Nachrichten zu finden, die den Kriterien entsprechen. Wenn dieses Flag nicht festgelegt ist, ist der CPU-intensive Teil des Suchvorgangs beendet. Dieses Flag hat nur eine Bedeutung, wenn die Suche aktiv ist (d. h. wenn SEARCH_RUNNING festgelegt ist).
    
SEARCH_RECURSIVE 
  
> Die Suche sucht in angegebenen Containern und allen untergeordneten Containern nach übereinstimmenden Einträgen. Wenn dieses Flag nicht festgelegt ist, werden nur die Container durchsucht, die explizit im letzten Aufruf der [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) enthalten sind. 
    
SEARCH_RUNNING 
  
> Die Suche ist aktiv, und die Inhaltstabelle des Containers wird aktualisiert, um Änderungen im Nachrichtenspeicher oder Adressbuch widerspiegeln zu können. Wenn dieses Flag nicht festgelegt ist, ist die Suche inaktiv und die Inhaltstabelle statisch.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Suchkriterien wurden erfolgreich ermittelt.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Suchkriterien wurden nie für den Container festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::GetSearchCriteria-Methode** ruft die Suchkriterien für einen Container ab, der Suchen unterstützt, in der Regel ein Suchergebnisordner. Sie erstellen Suchkriterien, indem Sie die **IMAPIContainer::SetSearchCriteria-Methode** eines Containers aufrufen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Adressbuchcontainer müssen **GetSearchCriteria** möglicherweise nur unterstützen, wenn sie die erweiterten Suchfunktionen bereitstellen, die der **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) -Eigenschaft zugeordnet sind. Weitere Informationen zum Implementieren des erweiterten Suchfeatures für Adressbuchcontainer finden Sie unter [Implementing Advanced Searching](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie mit den Datenstrukturen fertig sind, auf die die  _Parameter lppRestriction_ und  _lppContainerList_ zeigen, rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) einmal auf, damit jede Struktur freigegeben wird. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI verwendet die **IMAPIContainer::GetSearchCriteria-Methode,** um Suchkriterien aus einem angezeigten Ordner zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagSearch (kanonische Eigenschaft)](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 13c151a134e4334e8ed2e75e031a6fc9dddbf941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792075"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Betrifft**: Outlook 
  
Ruft die Suchkriterien für den Container an.
  
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
  
> [in] Eine Bitmaske aus Flags, die den Typ der übergebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lppRestriction_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert. Wenn eine Clientanwendung NULL im Parameter _LppRestriction_ erfolgreich ist, gibt **GetSearchCriteria** keine **SRestriction** -Struktur zurück. 
    
 _lppContainerList_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eintragsbezeichner, die Container, in die Suche einbezogen werden darstellen. Wenn ein Client NULL im Parameter _LppContainerList_ übergibt, gibt **GetSearchCriteria** ein Array von Eintragsbezeichner keine zurück. 
    
 _lpulSearchState_
  
> [out] Ein Zeiger auf eine Bitmaske aus Flags verwendet, um den aktuellen Status der Suche anzugeben. Wenn ein Client NULL im Parameter _LpulSearchState_ übergibt, gibt **GetSearchCriteria** keine Flags zurück. Die folgenden Kennzeichen können festgelegt werden: 
    
SEARCH_FOREGROUND 
  
> Die Suche sollte mit hoher Priorität relativ zu anderen Suchvorgänge ausgeführt. Wenn dieses Flag nicht festgelegt ist, wird die Suche mit normaler Priorität relativ zu anderen Suchvorgänge ausgeführt.
    
SEARCH_REBUILD 
  
> Die Suche ist im Modus CPU-intensiver ihren Funktionen, die versuchen, Nachrichten zu suchen, die den Kriterien entsprechen. Wenn dieses Flag nicht festgelegt ist, gehört die CPU-intensiver Vorgang für die Suche über. Dieses Kennzeichen wirkt sich nur, wenn die Suche aktiviert ist (d. h., wenn das Flag SEARCH_RUNNING festgelegt ist).
    
SEARCH_RECURSIVE 
  
> Die Suche wird in den angegebenen Container und deren untergeordnete Container für übereinstimmende Einträge suchen. Wenn dieses Flag nicht festgelegt ist, werden nur die explizit in den letzten Aufruf der [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode einbezogen Container durchsucht wird. 
    
SEARCH_RUNNING 
  
> Die Suche ist aktiv und Inhaltstabelle des Containers wird aktualisiert, um die Änderungen im Nachrichtenspeicher oder -Adressbuch. Wenn dieses Flag nicht festgelegt ist, wird die Suche ist deaktiviert, und der Inhaltstabelle ist statische.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Suchkriterien erfolgreich abgerufen wurde.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Nie wurden die Suchkriterien für den Container festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::GetSearchCriteria** -Methode ruft die Suchkriterien für einen Container, der sucht, in der Regel in einem Suchergebnisse Ordner unterstützt. Erstellen Sie Suchkriterien durch Aufrufen des Containers **IMAPIContainer::SetSearchCriteria** -Methode. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Address Book Containern müssen möglicherweise **GetSearchCriteria** unterstützen nur, wenn die erweiterte Suche-Funktionen der Eigenschaft **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) zugeordnet bieten. Weitere Informationen zum Implementieren die erweiterten Suchfunktion für Address Book Container, finden Sie unter [Implementieren der erweiterten Suche](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie mit den Datenstrukturen auf das durch die Parameter _LppRestriction_ und _LppContainerList_ abgeschlossen haben, rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) einmal für jede Struktur freigegeben werden muss. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI (engl.) verwendet die **IMAPIContainer::GetSearchCriteria** -Methode, um Suchkriterien aus einem Ordner anzuzeigenden abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Kanonische PidTagSearch-Eigenschaft](pidtagsearch-canonical-property.md)
  
[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426198"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf die Hierarchietabelle des Containers zurück.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie Informationen in der Tabelle zurückgegeben werden. Die folgenden Flags können festgelegt werden:
    
CONVENIENT_DEPTH 
  
> Füllt die Hierarchietabelle mit Containern aus mehreren Ebenen. Wenn CONVENIENT_DEPTH nicht festgelegt ist, enthält die Hierarchietabelle nur die unmittelbaren untergeordneten Containern des Behälters.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchy** kann erfolgreich zurückgegeben werden, möglicherweise bevor die Tabelle dem Aufrufer zur Verfügung gestellt wird. Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellen Aufruf ein Fehler ausgelöst werden. 
    
MAPI_UNICODE 
  
> Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als weich gelöscht markiert sind, d. h., Sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Hierarchietabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Hierarchietabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container verfügt über keine untergeordneten Container und kann keine Hierarchietabelle bereitstellen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer:: GetHierarchy** -Methode gibt einen Zeiger auf die Hierarchietabelle eines Containers zurück. Eine Hierarchietabelle enthält zusammenfassende Informationen zu den untergeordneten Containern im Container. Ordner Hierarchietabellen enthalten Informationen zu Unterordnern; Adressbuch-Hierarchietabellen enthalten Informationen zu untergeordneten Adressbuch Containern und Verteilerlisten. 
  
Für einige Container ist es möglich, keine untergeordneten Container zu haben. Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen **** von gethierarchyid zurück.
  
Wenn das CONVENIENT_DEPTH-Flag festgelegt ist, enthält jede Zeile in der Hierarchietabelle auch die **PR_DEPTH** ([pidtagdepth (](pidtagdepth-canonical-property.md))-Eigenschaft als Spalte. **PR_DEPTH** gibt die Ebene der einzelnen Container relativ zu dem Container an, der die Tabelle implementiert. Die unmittelbaren untergeordneten Container des implementierenden Containers befinden sich in der Tiefe Null, untergeordnete Container in den Containern mit der Tiefe 1 und so weiter. Die Werte von **PR_DEPTH** werden sequenziell erhöht, wenn sich die Hierarchie der Ebenen vertieft. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in den Hierarchietabellen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie eine Hierarchietabelle für ihren Container unterstützen, müssen Sie auch die folgenden Schritte ausführen:
  
- Unterstützen Sie einen Aufruf der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers, um die **PR_CONTAINER_HIERARCHY** ([pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))-Eigenschaft zu öffnen.
    
- Zurückgeben von **PR_CONTAINER_HIERARCHY** von einem Aufruf der [IMAPIProp::](imapiprop-getproplist.md) getproplist-oder [IMAPIProp::](imapiprop-getprops.md) GetProps-Methoden des Containers. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Tabellenspalten für String-und Binary-Inhalte können abgeschnitten werden. In der Regel geben Anbieter 255 Zeichen zurück. Da Sie nicht vorher wissen können, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 255 oder 510 Byte beträgt. Sie können den vollständigen Wert einer abgeschnittenen Spalte, falls erforderlich, jederzeit direkt aus dem Objekt abrufen, indem Sie die Eintrags-ID verwenden, um Sie zu öffnen und dann die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode aufzurufen. 
  
Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge auf die gesamte Zeichenfolge oder auf die gekürzte Version dieser Zeichenfolge angewendet werden. Darüber hinaus werden die für die Hierarchietabellen angegebenen [SSortOrderSet](ssortorderset.md) für Speicheranbieter nicht unbedingt berücksichtigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl. cpp  <br/> |CHierarchyTableTreeCtrl:: getHierarchy.  <br/> |Die CHierarchyTableTreeCtrl-Klasse **** verwendet gethierarchyable, um Hierarchietabellen abzurufen, die in einem Strukturansicht-Steuerelement angezeigt werden sollen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Kanonische Pidtagcontainerhierarchy (-Eigenschaft](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


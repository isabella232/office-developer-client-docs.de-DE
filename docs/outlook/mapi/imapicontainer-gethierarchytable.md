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
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563800"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf den Container Hierarchietabelle.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie Informationen in der Tabelle zurückgegeben werden. Die folgenden Kennzeichen können festgelegt werden:
    
CONVENIENT_DEPTH 
  
> Füllt die Hierarchietabelle mit Container mit Daten aus mehreren Ebenen. Wenn CONVENIENT_DEPTH nicht festgelegt ist, enthält die Hierarchietabelle nur den Container direkt untergeordnete Container.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** können erfolgreich, möglicherweise beendet, bevor die Tabelle mit dem Anrufer verfügbar gemacht wird. Wenn die Tabelle nicht verfügbar ist, kann die nachfolgenden Tabelle Anrufen ein Fehler ausgelöst. 
    
PARAMETER MAPI_UNICODE 
  
> Anforderungen, die die Spalten, die Zeichenfolgendaten enthalten im Unicode-Format zurückgegeben werden soll. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Hierarchietabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Hierarchietabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container hat keine untergeordnete Container und keine Hierarchietabelle bereitstellen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIContainer::GetHierarchyTable** -Methode gibt einen Zeiger auf die Hierarchietabelle eines Containers. Eine Hierarchietabelle enthält zusammenfassende Informationen zu der untergeordnete Container im Container. Ordner Hierarchietabellen enthalten Informationen über Unterordner; Address Book Hierarchietabellen enthalten Informationen über untergeordnete Address Book Container und Verteilerlisten. 
  
Es ist möglich, dass einige Container haben keine untergeordnete Container. Diese Container zurück MAPI_E_NO_SUPPORT aus ihrer Implementierungen von **GetHierarchyTable**.
  
Wenn das Flag CONVENIENT_DEPTH festgelegt ist, enthält jede Zeile in der Hierarchietabelle die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft auch als Spalte. **PR_DEPTH** gibt die Ebene der einzelnen Container relativ zum Container, der die Tabelle implementiert. Implementieren des Containers direkt untergeordnetes Element, für den Container Tiefe 0 (null), untergeordnete Container in NULL Tiefe Container sind finden Sie auf eine Tiefe usw.. Die Werte der **PR_DEPTH** sequenziell erhöht, wie die Hierarchie der Ebenen – Revcovery. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in Hierarchietabellen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie eine Hierarchietabelle für den Container unterstützen, müssen Sie auch Folgendes:
  
- Unterstützung von einem Aufruf des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))-Eigenschaft.
    
- Geben Sie einen Anruf an den Container [IMAPIProp::GetPropList](imapiprop-getproplist.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md) Methoden **PR_CONTAINER_HIERARCHY** zurück. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zeichenfolge und der binären Inhalt Tabellenspalten können abgeschnitten werden. In der Regel zurückgeben Anbieter 255 Zeichen. Da Sie im Voraus wissen können nicht, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen Sie, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 510 maximal 255 Bytes ist. Sie können immer den vollständigen Wert der abgeschnittene Spalte an, falls erforderlich, direkt aus dem Objekt mithilfe der Eintrags-ID um zu öffnen und anschließendes Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abrufen. 
  
Je nach der Implementierung des Anbieters, Einschränkungen und Sortierung Vorgänge können auf die gesamte Zeichenfolge oder auf die abgeschnittene Version dieser Zeichenfolge anwenden. Darüber hinaus sind Anbieter nicht unbedingt festgelegten Reihenfolge sortieren berücksichtigt, [SSortOrderSet](ssortorderset.md) für Hierarchietabellen angegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |Die CHierarchyTableTreeCtrl-Klasse wird mit **GetHierarchyTable** Hierarchietabellen anzeigen in einem Strukturansicht-Steuerelement abgerufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


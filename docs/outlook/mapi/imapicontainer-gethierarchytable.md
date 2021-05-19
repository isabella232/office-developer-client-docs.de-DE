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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Informationen in der Tabelle zurückgegeben werden. Die folgenden Kennzeichen können festgelegt werden:
    
CONVENIENT_DEPTH 
  
> Füllt die Hierarchietabelle mit Containern aus mehreren Ebenen. Wenn CONVENIENT_DEPTH festgelegt ist, enthält die Hierarchietabelle nur die unmittelbar untergeordneten Container des Containers.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** kann erfolgreich zurückgeben, möglicherweise bevor die Tabelle dem Aufrufer zur Verfügung steht. Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellenaufruf ein Fehler verursacht werden. 
    
MAPI_UNICODE 
  
> Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden. Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als "soft deleted" gekennzeichnet sind, d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Hierarchietabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Hierarchietabelle wurde erfolgreich abgerufen.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Der Container verfügt über keine untergeordneten Container und kann keine Hierarchietabelle bereitstellen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::GetHierarchyTable-Methode** gibt einen Zeiger auf die Hierarchietabelle eines Containers zurück. Eine Hierarchietabelle enthält Zusammenfassende Informationen zu den untergeordneten Containern im Container. Ordnerhierarchietabellen enthalten Informationen zu Unterordnern. Adressbuchhierarchietabellen enthalten Informationen zu untergeordneten Adressbuchcontainern und Verteilerlisten. 
  
Es ist möglich, dass einige Container keine untergeordneten Container haben. Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen von **GetHierarchyTable zurück.**
  
Wenn das CONVENIENT_DEPTH festgelegt ist, enthält jede Zeile in der Hierarchietabelle auch die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) -Eigenschaft als Spalte. **PR_DEPTH** gibt die Ebene der einzelnen Container relativ zum Container an, der die Tabelle implementiert. Die unmittelbaren untergeordneten Container des implementierende Containers befinden sich in der Tiefe Null, untergeordnete Container in den Containern mit null Tiefe befinden sich in der ersten Tiefe und so weiter. Die Werte der **PR_DEPTH** werden sequentiell erhöht, wenn sich die Hierarchie der Ebenen erhöht. 
  
Eine vollständige Liste der erforderlichen und optionalen Spalten in Hierarchietabellen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Sie eine Hierarchietabelle für Ihren Container unterstützen, müssen Sie auch die folgenden Schritte tun:
  
- Unterstützen Sie einen Aufruf der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des **Containers,** um die PR_CONTAINER_HIERARCHY ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) -Eigenschaft zu öffnen.
    
- Geben **PR_CONTAINER_HIERARCHY** von einem Aufruf der [METHODEN IMAPIProp::GetPropList](imapiprop-getproplist.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md) des Containers zurück. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Tabellenspalten mit Zeichenfolgen und binären Inhalten können abgeschnitten werden. In der Regel geben Anbieter 255 Zeichen zurück. Da Sie vorher nicht wissen können, ob eine Tabelle abgeschnittene Spalten enthält, nehmen Sie an, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte entweder 255 oder 510 Byte beträgt. Sie können jederzeit den vollständigen Wert einer abgeschnittenen Spalte bei Bedarf direkt aus dem Objekt abrufen, indem Sie den Eintragsbezeichner zum Öffnen verwenden und dann die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) aufrufen. 
  
Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge auf die gesamte Zeichenfolge oder die gekürzte Version dieser Zeichenfolge angewendet werden. Darüber hinaus ist es nicht garantiert, dass Speicheranbieter den für Hierarchietabellen angegebenen [Sortierreihenfolgensatz SSortOrderSet](ssortorderset.md) berücksichtigt. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |Die CHierarchyTableTreeCtrl-Klasse verwendet **GetHierarchyTable,** um Hierarchietabellen zum Anzeigen in einem Strukturansichtssteuerelement zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerHierarchy (kanonische Eigenschaft)](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)


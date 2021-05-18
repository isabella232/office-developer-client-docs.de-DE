---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422894"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft alle Zeilen einer Tabelle ab. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a>Parameter

 _ptable_
  
> [in] Zeiger auf die MAPI-Tabelle, aus der Zeilen abgerufen werden. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die Tabellenspalten angeben. Diese Tags werden verwendet, um die spezifischen Spalten auszuwählen, die abgerufen werden sollen. Wenn der  _ptaga-Parameter_ NULL ist, **ruft HrQueryAllRows** den gesamten Spaltensatz der aktuellen Tabellenansicht ab, die im  _ptable-Parameter übergeben_ wird. 
    
 _pres_
  
> [in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die Abrufeinschränkungen enthält. Wenn der  _parameter pres_ NULL ist, **macht HrQueryAllRows** keine Einschränkungen. 
    
 _psos_
  
> [in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die Sortierreihenfolge der abzurufenden Spalten identifiziert. Wenn der  _psos-Parameter_ NULL ist, wird die Standardsortierungsreihenfolge für die Tabelle verwendet. 
    
 _krähenMax_
  
> [in] Maximale Anzahl der abzurufende Zeilen. Wenn der Wert des  _Parameters "krähenMax"_ null ist, wird kein Grenzwert für die Anzahl der abgerufenen Zeilen festgelegt. 
    
 _pprows_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [SRowSet-Struktur,](srowset.md) die ein Array von Zeigern auf die abgerufenen Tabellenzeilen enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf hat die erwarteten Zeilen einer Tabelle abgerufen. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Die Anzahl der Zeilen in der Tabelle ist größer als die für den  _Parameter "krähenMax" übergebene_ Anzahl. 
    
## <a name="remarks"></a>Hinweise

Eine Clientanwendung oder ein Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** abzurufen versucht, es sei denn, es wird eine Einschränkung festgelegt, auf die der  _parameter pres_ verweist. Der  _parameter "krähesMax"_ begrenzt den Abruf nicht auf eine bestimmte Anzahl von Tabellenzeilen, sondern definiert eine maximale Menge an Arbeitsspeicher, die für alle abgerufenen Zeilen verfügbar ist. Der einzige Schutz vor massivem Speicherüberlauf ist das Stopgap-Feature, das durch Festlegen von _"krähenMax" bereitgestellt wird._ Der Fehlerrücklauf MAPI_E_TABLE_TOO_BIG bedeutet, dass die Tabelle zu viele Zeilen enthält, um alle gleichzeitig im Arbeitsspeicher gespeichert zu werden. 
  
Tabellen, die in der Regel klein sind, z. B. eine Nachrichtenspeichertabelle oder eine Anbietertabelle, können in der Regel mit **HrQueryAllRows** sicher abgerufen werden. Tabellen, bei der das Risiko besteht, dass sie sehr groß sind, z. B. eine Inhaltstabelle oder sogar eine Empfängertabelle, sollten mithilfe der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) in Unterabschnitten durchlaufen werden. 
  
Wenn Tabelleneigenschaften nicht definiert sind, wenn **HrQueryAllRows** aufgerufen wird, werden sie mit dem Eigenschaftentyp PT_NULL und eigenschaftsbezeichner PROP_ID_NULL 
  


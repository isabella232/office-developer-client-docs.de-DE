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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348244"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft alle Zeilen einer Tabelle ab. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf die MAPI-Tabelle, aus der die Zeilen abgerufen werden. 
    
 _ptaga_
  
> in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die Tabellenspalten anzeigen. Diese Tags werden verwendet, um die einzelnen Spalten auszuwählen, die abgerufen werden sollen. Wenn der _ptaga_ -Parameter NULL ist, ruft **HrQueryAllRows** den gesamten Spaltensatz der aktuellen Tabellenansicht ab, die im _ptable_ -Parameter übergeben wird. 
    
 _Pres_
  
> in Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die Abruf Einschränkungen enthält. Wenn der _Pres_ -Parameter NULL ist, macht **HrQueryAllRows** keine Einschränkungen. 
    
 _PSOs_
  
> in Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge der Spalten angibt, die abgerufen werden sollen. Wenn der __ Parameter "Parameters" den Wert NULL hat, wird die Standardsortierreihenfolge für die Tabelle verwendet. 
    
 _crowsMax_
  
> in Maximale Anzahl von Zeilen, die abgerufen werden sollen. Wenn der Wert des _crowsMax_ -Parameters 0 (null) ist, wird kein Grenzwert für die Anzahl der abgerufenen Zeilen festgelegt. 
    
 _pprows_
  
> Out Zeiger auf einen Zeiger auf die zurückgegebene [SRowSet](srowset.md) -Struktur, die ein Array von Zeigern auf die abgerufenen Tabellenzeilen enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf hat die erwarteten Zeilen einer Tabelle abgerufen. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Die Anzahl der Zeilen in der Tabelle ist größer als die Anzahl, die für den _crowsMax_ -Parameter übergeben wurde. 
    
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder ein Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** abruft, außer durch eine Einschränkung, auf die durch den _Pres_ -Parameter verwiesen wird. Der Parameter _crowsMax_ schränkt den Abruf nicht auf eine bestimmte Anzahl von Tabellenzeilen ein, sondern definiert eine maximale Menge an Arbeitsspeicher, die für alle abgerufenen Zeilen verfügbar ist. Der einzige Schutz vor massivem Speicherüberlauf ist das durch Festlegen von _crowsMax_bereitgestellte Notlösung-Feature. Der Fehler Return MAPI_E_TABLE_TOO_BIG gibt an, dass die Tabelle zu viele Zeilen enthält, die alle gleichzeitig im Arbeitsspeicher aufbewahrt werden sollen. 
  
Tabellen, die normalerweise klein sind, wie beispielsweise eine Nachrichtenspeichertabelle oder eine Anbieter Tabelle, können mit **HrQueryAllRows**in der Regel sicher abgerufen werden. Tabellen, die sehr umfangreich sind, wie beispielsweise eine Inhaltstabelle oder sogar eine Empfängertabelle, sollten mithilfe der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode in Unterabschnitten durchlaufen werden. 
  
Wenn Tabelleneigenschaften nicht definiert sind, wenn **HrQueryAllRows** aufgerufen wird, werden Sie mit dem Eigenschaftentyp PT_NULL und dem EIGENSCHAFTENbezeichner PROP_ID_NULL 
  


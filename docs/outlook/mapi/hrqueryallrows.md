---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea4e22a379943429476368ca09e37db5caa8e593
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561600"
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

 _Ptable_
  
> [in] Zeiger auf die MAPI-Tabelle, aus der Zeilen abgerufen werden. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die Tabellenspalten angeben. Diese Tags werden verwendet, um die spezifischen Spalten auszuwählen, die abgerufen werden sollen. Wenn der  _Ptaga-Parameter_ NULL ist, ruft **HrQueryAllRows** den gesamten Spaltensatz der aktuellen Tabellenansicht ab, der im  _ptable-Parameter_ übergeben wird. 
    
 _Pres_
  
> [in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die Abrufeinschränkungen enthält. Wenn der  _Pres-Parameter_ NULL ist, macht **HrQueryAllRows** keine Einschränkungen. 
    
 _Psos_
  
> [in] Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die Sortierreihenfolge der abzurufenden Spalten identifiziert. Wenn der  _Psos-Parameter_ NULL ist, wird die Standardsortierreihenfolge für die Tabelle verwendet. 
    
 _-Max_
  
> [in] Maximale Anzahl der abzurufenden Zeilen. Wenn der Wert des  _Parameters "rowssMax"_ null ist, wird kein Grenzwert für die Anzahl der abgerufenen Zeilen festgelegt. 
    
 _Pprows_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [SRowSet-Struktur,](srowset.md) die ein Array von Zeigern auf die abgerufenen Tabellenzeilen enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf hat die erwarteten Zeilen einer Tabelle abgerufen. 
    
MAPI_E_TABLE_TOO_BIG 
  
> Die Anzahl der Zeilen in der Tabelle ist größer als die Anzahl, die für den  _Parameter "widthsMax"_ übergeben wird. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung oder ein Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** abzurufen versucht, außer durch das Aufheben einer Einschränkung, auf die der  _Parameter "pres"_ verweist. Der  _Parameter "widthsMax"_ beschränkt den Abruf nicht auf eine bestimmte Anzahl von Tabellenzeilen, sondern definiert eine maximale Speichermenge, die für alle abgerufenen Zeilen verfügbar ist. Der einzige Schutz vor massivem Speicherüberlauf ist die Stopgap-Funktion, die durch Festlegen von  _"WarteschlangenMax"_ bereitgestellt wird. The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be all at once in memory. 
  
Tabellen, die in der Regel klein sind, z. B. eine Nachrichtenspeichertabelle oder eine Anbietertabelle, können in der Regel mit **HrQueryAllRows** sicher abgerufen werden. Tabellen mit dem Risiko, sehr groß zu sein, z. B. ein Inhaltsverzeichnis oder sogar eine Empfängertabelle, sollten in Unterabschnitten mithilfe der [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) durchlaufen werden. 
  
Wenn Tabelleneigenschaften beim Aufrufen von **HrQueryAllRows** nicht definiert sind, werden sie mit eigenschaftstyp PT_NULL und Eigenschaftenbezeichner zurückgegeben PROP_ID_NULL 
  


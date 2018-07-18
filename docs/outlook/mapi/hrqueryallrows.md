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
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791940"
---
# <a name="hrqueryallrows"></a>HrQueryAllRows

  
  
**Betrifft**: Outlook 
  
Ruft alle Zeilen einer Tabelle ab. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf die MAPI-Tabelle aus der Zeilen abgerufen werden. 
    
 _ptaga_
  
> [in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array der-Eigenschaft enthält tags Tabellenspalten angibt. Diese Tags dienen zum Auswählen der spezifischen Spalten abgerufen werden sollen. Wenn der Parameter _Ptaga_ NULL ist, ruft **HrQueryAllRows** den gesamte Spaltensatz von der aktuellen Tabellenansicht im _Ptable_ -Parameter übergeben. 
    
 _Pres_
  
> [in] Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die Retrieval Einschränkungen enthält. Wenn der Parameter _Pres_ NULL ist, wird **HrQueryAllRows** ohne Einschränkungen. 
    
 _PSOs_
  
> [in] Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, identifiziert die Sortierreihenfolge der Spalten abgerufen werden sollen. Wenn der Parameter _Psos_ NULL ist, wird die standardmäßige Sortierreihenfolge für die Tabelle verwendet. 
    
 _crowsMax_
  
> [in] Maximale Anzahl von Zeilen abgerufen werden sollen. Wenn der Wert des Parameters _CrowsMax_ gleich NULL ist, wird keine Begrenzung für die Anzahl der abgerufenen Zeilen festgelegt. 
    
 _ppRows_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene [SRowSet](srowset.md) -Struktur, die ein Array von Zeigern für die abgerufenen Zeilen enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Anruf abgerufen, die erwarteten Zeilen einer Tabelle. 
    
KEINE 
  
> Die Anzahl der Zeilen in der Tabelle ist größer als die Anzahl für den _CrowsMax_ -Parameter übergeben. 
    
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder Dienstanbieter hat keine Kontrolle über die Anzahl der Zeilen, die **HrQueryAllRows** versucht, abrufen, außer durch die Festlegung einer Einschränkung mit durch den Parameter _Pres_ gezeigt. Der Parameter _CrowsMax_ schränkt nicht das Abrufen auf eine bestimmte Anzahl von Zeilen der Tabelle, aber vielmehr definiert eine maximale Größe des Arbeitsspeichers zur Verfügung, die alle abgerufene Zeilen enthalten soll. Der einzige Schutz gegen Speicher Überlauf ist die stetig Funktion _CrowsMax_festlegen. Die Rendite der Fehler, die bedeutet, die Tabelle dass enthält zu viele Zeilen, die alle gleichzeitig im Speicher aufbewahrt werden. 
  
Tabellen, die in der Regel klein, wie eine Nachricht Store Tabelle oder einer Tabelle Anbieter können in der Regel sicher mit **HrQueryAllRows**abgerufen werden. Tabellen Risiko, wird sehr groß sein, wie etwa eine Inhalt oder sogar eine Tabelle Empfänger, sollte in [der QueryRows](imapitable-queryrows.md) mit Unterabschnitten durchlaufen werden. 
  
Wenn alle Tabelleneigenschaften **HrQueryAllRows** aufgerufen wird nicht definiert sind, werden diese mit Eigenschaftentyp PT_NULL und Eigenschaftenbezeichner PROP_ID_NULL zurückgegeben. 
  


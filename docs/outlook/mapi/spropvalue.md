---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795626"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Betrifft**: Outlook 
  
Beschreibt eine MAPI-Eigenschaft.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [eigensch_id](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Elemente

 **ulPropTag**
  
> Eigenschaftentag für die Eigenschaft. Eigenschaftentags sind nicht signierte 32-Bit-Ganzzahl bestehend aus der Eigenschaftenbezeichner in die obere 16-Bit und den Typ der Eigenschaft in den niederwertige 16 Bit.
    
 **dwAlignPad**
  
> Reserviert für die MAPI. Verwenden Sie nicht. 
    
 **Wert**
  
> Union von Datenwerten, die bestimmten Wert durch den Eigenschaftentyp vorgegeben. Die folgende Tabelle enthält für jeden Eigenschaftentyp, das Mitglied der Union, die verwendet werden soll und dem entsprechenden Datentyp.
    
|**Eigenschaftstyp**|**Wert**|**Datentyp des Werts**|
|:-----|:-----|:-----|
|PT_I2 oder PT_SHORT  <br/> |**Ich** <br/> |kurze int  <br/> |
|PT_I4 oder PT_LONG (mit Vorzeichen)  <br/> |**l** <br/> |LANGE  <br/> |
|PT_I4 oder PT_LONG (ohne Vorzeichen)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 oder PT_FLOAT  <br/> |**flt** <br/> |Gleitkommazahl  <br/> |
|PT_R8 oder PT_DOUBLE  <br/> |**Doppelte Japan** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |nicht signierte kurze int  <br/> |
|PT_CURRENCY  <br/> |**Übernehmen** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**unter** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Papierkorb** <br/> |[BYTEARRAYS]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**x lpguid** <br/> |X LPGUID  <br/> |
|PT_I8 oder PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL oder PT_OBJECT  <br/> |**x** <br/> |LANGE  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Element **UlPropTag** besteht aus zwei Teilen: 
  
- Ein Bezeichner in der hohen 16 Bits.
    
- Ein Typ in den niederwertige 16 Bit.
    
Der Bezeichner ist einen numerischen Wert in einem bestimmten Bereich. MAPI definiert Bereiche für Bezeichner zum Beschreiben der für die-Eigenschaft verwendet wird und die, die für die Verwaltung zuständig ist. MAPI definiert Einschränkungen für jede Eigenschaft Tags, die sie in der Headerdatei Mapitags.h unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft. MAPI definiert Konstanten für jede Eigenschaftentypen, die in der Headerdatei Mapidefs.h unterstützt. 
  
Eine vollständige Liste der Bereiche gültige Eigenschaft für Bezeichner und Eigenschaftentypen finden Sie im Anhang [Eigenschaftenbezeichner und Typen](property-identifiers-and-types.md) . 
  
Das **DwAlignPad** -Element wird als Abstand verwendet, um sicherzustellen, dass ordnungsgemäße Ausrichtung auf Computern erstellen, die 8-Byte-Ausrichtung für 8-Byte-Wert erforderlich ist. Entwickler, die auf solchen Computern Code schreiben sollten Memory Allocation Routinen verwenden, die die **SPropValue** Arrays auf 8-Byte-Grenzen zuweisen. 
  
Weitere Informationen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md) und [Aktualisieren von MAPI-Eigenschaften](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)


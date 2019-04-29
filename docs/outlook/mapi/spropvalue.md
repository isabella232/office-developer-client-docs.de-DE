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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433528"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine MAPI-Eigenschaft.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verwandte Makros:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> Property-Tag für die Eigenschaft. Eigenschaftstags sind 32-Bit-Ganzzahlen ohne Vorzeichen, bestehend aus dem eindeutigen Bezeichner der Eigenschaft in den hochwertigen 16 Bits und dem Typ der Eigenschaft in den niedrigwertigen 16 Bits.
    
 **dwAlignPad**
  
> Reserviert für MAPI; nicht verwenden. 
    
 **Wert**
  
> Vereinigung von Datenwerten, der spezifische Wert, der vom Eigenschaftentyp diktiert wird. In der folgenden Tabelle werden die einzelnen Eigenschaftentypen, das zu verwendende Mitglied der Union und der zugehörige Datentyp aufgeführt.
    
|**Eigenschaftentyp**|**Wert**|**Datentyp des Werts**|
|:-----|:-----|:-----|
|PT_I2 oder PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 oder PT_LONG (signiert)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 oder PT_LONG (unsigned)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 oder PT_FLOAT  <br/> |**FLT** <br/> |Gleitkommazahl  <br/> |
|PT_R8 oder PT_DOUBLE  <br/> |**Doppel** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**auf** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [Array]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 oder PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVbei** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL oder PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **ulPropTag** -Element besteht aus zwei Teilen: 
  
- Ein Bezeichner in den hochwertigen 16 Bits.
    
- Ein Typ in den niederwertigen 16 Bits.
    
Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist. MAPI definiert Einschränkungen für die einzelnen Eigenschaftentags, die in der Headerdatei Mapitags. h unterstützt werden.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für alle Eigenschaftentypen, die in der Headerdatei Mapidefs. h unterstützt werden. 
  
Eine vollständige Liste der gültigen Eigenschaftsbereiche für Bezeichner und Eigenschaftentypen finden Sie unter der [Eigenschaftsbezeichner und-Typen](property-identifiers-and-types.md) . 
  
Das **dwAlignPad** -Element wird als Textabstand verwendet, um eine ordnungsgemäße Ausrichtung auf Computern sicherzustellen, die eine 8-Byte-Ausrichtung für 8-Byte-Werte erfordern. Entwickler, die Code auf solchen Computern schreiben, sollten Speicher Zuordnungs Routinen verwenden, die die **SPropValue** -Arrays an 8-Byte-Begrenzungen zuweisen. 
  
Weitere Informationen finden Sie unter [Übersicht über MAPI-Eigenschaftentypen](mapi-property-type-overview.md) und [Aktualisieren von MAPI-Eigenschaften](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)


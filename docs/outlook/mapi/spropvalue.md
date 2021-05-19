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
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
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
  
> Eigenschaftstag für die Eigenschaft. Eigenschaftstags sind 32-Bit-ganzzahlige, nicht signierte Ganzzahlen, die aus dem eindeutigen Bezeichner der Eigenschaft in der hohen Reihenfolge von 16 Bit und dem Typ der Eigenschaft in der niedrigen Reihenfolge von 16 Bit bestehen.
    
 **dwAlignPad**
  
> Reserviert für MAPI; nicht verwenden. 
    
 **Wert**
  
> Union der Datenwerte, der vom Eigenschaftentyp diktierte spezifische Wert. In der folgenden Tabelle sind die einzelnen Eigenschaftentypen, das Zu verwendende Mitglied der Union und der zugehörige Datentyp aufgeführt.
    
|**Eigenschaftentyp**|**Wert**|**Datentyp value**|
|:-----|:-----|:-----|
|PT_I2 oder PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 oder PT_LONG (signiert)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 oder PT_LONG (nicht signiert)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 oder PT_FLOAT  <br/> |**flt** <br/> |Gleitkommazahl  <br/> |
|PT_R8 oder PT_DOUBLE  <br/> |**dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**at** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [array]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
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
|PT_NULL oder PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID \*  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **ulPropTag-Element** besteht aus zwei Teilen: 
  
- Ein Bezeichner in der hohen Reihenfolge von 16 Bit.
    
- Ein Typ in niedriger Reihenfolge von 16 Bit.
    
Der Bezeichner ist ein numerischer Wert innerhalb eines bestimmten Bereichs. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für die Verwaltung verantwortlich ist. MAPI definiert Einschränkungen für jedes der Eigenschaftentags, die es in der Mapitags.h-Headerdatei unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden. 
  
Eine vollständige Liste der gültigen Eigenschaftsbereiche für Bezeichner und Eigenschaftstypen finden Sie im Anhang [Property Identifiers and Types.](property-identifiers-and-types.md) 
  
Das **dwAlignPad-Element** wird als Abstand verwendet, um die ordnungsgemäße Ausrichtung auf Computern sicherzustellen, für die eine 8-Byte-Ausrichtung für 8-Byte-Werte erforderlich ist. Entwickler, die Code auf solchen Computern schreiben, sollten Speicherzuweisungsroutinen verwenden, die **die SPropValue-Arrays** an 8-Byte-Grenzen zuordnen. 
  
Weitere Informationen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)


---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0b26c5d0ef2906945becbfe4dd121d10831ca05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566528"
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

## <a name="members"></a>Members

 **ulPropTag**
  
> Eigenschaftstag für die Eigenschaft. Eigenschaftstags sind 32-Bit-Ganzzahlen ohne Vorzeichen, die aus dem eindeutigen Bezeichner der Eigenschaft in den 16 Bit in hoher Reihenfolge und dem Typ der Eigenschaft in der unteren Reihenfolge von 16 Bit bestehen.
    
 **wetterAlignPad**
  
> Reserviert für MAPI; nicht verwenden. 
    
 **Wert**
  
> Vereinigung von Datenwerten, der durch den Eigenschaftstyp vorgegebene spezifische Wert. In der folgenden Tabelle sind die einzelnen Eigenschaftstypen, das Zu verwendende Mitglied der Vereinigung und der zugeordnete Datentyp aufgeführt.
    
|**Eigenschaftentyp**|**Wert**|**Datentyp des Werts**|
|:-----|:-----|:-----|
|PT_I2 oder PT_SHORT  <br/> |**Ich** <br/> |short int  <br/> |
|PT_I4 oder PT_LONG (signiert)  <br/> |**l** <br/> |LANGE  <br/> |
|PT_I4 oder PT_LONG (nicht signiert)  <br/> |**Ul** <br/> |ULONG  <br/> |
|PT_R4 oder PT_FLOAT  <br/> |**Flt** <br/> |Gleitkommazahl  <br/> |
|PT_R8 oder PT_DOUBLE  <br/> |**Dz** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**B** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**Cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**Auf** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**Ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Bin** <br/> |BYTE [Array]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 oder PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**Mvi** <br/> |[SShortArray](sshortarray.md) <br/> |
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
|PT_PTR  <br/> |**lpv** <br/> |LEERE \*  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **ulPropTag-Element** besteht aus zwei Teilen: 
  
- Ein Bezeichner in der hohen Reihenfolge von 16 Bit.
    
- Ein Typ in der niedrigen Reihenfolge von 16 Bit.
    
Der Bezeichner ist ein numerischer Wert innerhalb eines bestimmten Bereichs. MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist. MAPI definiert Einschränkungen für jedes der Eigenschaftstags, die es in der Mapitags.h-Headerdatei unterstützt.
  
Der Typ gibt das Format für den Wert der Eigenschaft an. MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden. 
  
Eine vollständige Liste der gültigen Eigenschaftenbereiche für Bezeichner und Eigenschaftstypen finden Sie im Anhang zu [Eigenschaftsbezeichnern und -typen.](property-identifiers-and-types.md) 
  
Das **element "wetterAlignPad"** wird als Abstand verwendet, um eine ordnungsgemäße Ausrichtung auf Computern sicherzustellen, die eine 8-Byte-Ausrichtung für 8-Byte-Werte erfordern. Entwickler, die Code auf solchen Computern schreiben, sollten Speicherzuweisungsroutinen verwenden, die die **SPropValue-Arrays** auf 8-Byte-Begrenzungen zuordnen. 
  
Weitere Informationen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Strukturen](mapi-structures.md)


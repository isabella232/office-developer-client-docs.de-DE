---
title: Eigenschaftentypen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407053"
---
# <a name="property-types"></a>Eigenschaftentypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI unterstützt sowohl einwertige als auch mehrwertige Eigenschaften. Bei einer einwertigen Eigenschaft gibt es einen Wert des Basistyps für die-Eigenschaft. Bei einer mehrwertigen Eigenschaft gibt es mehrere Werte des Basistyps. 
  
Die von MAPI unterstützten Eigenschaftentypen mit einem oder mehreren Werten werden in der folgenden Tabelle beschrieben. Für jeden einwertigen Typ, der über einen entsprechenden mehrwertigen Typ verfügt, wird der mehrwertige Typ in Klammern nach dem einwertigen Typ angezeigt.
  
|**Eigenschaftstyp**|**Hex-Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Gibt an, dass der Eigenschaftentyp unbekannt ist. Dieser Eigenschaftentyp ist für die Verwendung mit Schnittstellenmethoden reserviert.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Gibt keinen Eigenschaftswert an. Dieser Eigenschaftentyp ist für die Verwendung mit Schnittstellenmethoden reserviert und entspricht dem OLE-Typ VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Signierte 16-Bit-Ganzzahl (2-Byte). Dieser Eigenschaftentyp ist identisch mit PT_SHORT (PT_MV_SHORT) und dem OLE-Typ VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Signierte oder nicht signierte 32-Bit-Ganzzahl (4-Byte). Dieser Eigenschaftentyp ist identisch mit PT_LONG (PT_MV_LONG) und dem OLE-Typ VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32-Bit (8-Byte) Gleitkommawert. Dieser Eigenschaftentyp ist identisch mit PT_R4 (PT_MV_R4) und dem OLE-Typ VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64-Bit (8-Byte) Gleitkommawert. Dieser Eigenschaftentyp ist identisch mit PT_R8 und den OLE-Typen VT_R8 und VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64-Bit-Ganzzahl (8 Byte), interpretiert als Decimal. Dieser Eigenschaftentyp ist mit dem Microsoft Visual Basic-WÄHRUNGStyp kompatibel und entspricht dem OLE-Typ VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Double-Wert, der als Datum und Uhrzeit interpretiert wird. Der ganzzahligen Teil ist das Datum und das zu rundende Teil ist die Zeit. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_DATE und ist mit der Microsoft Visual Basic-Zeitdarstellung kompatibel.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE-Wert; 32-Bit-Ganzzahl (4 Byte) ohne Vorzeichen. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16-Bit-boolescher Wert (2 Byte), wobei null gleich **false** und ungleich NULL gleich **true**ist. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Zeiger auf ein Objekt, das die **IUnknown** -Schnittstelle implementiert. Dieser Eigenschaftentyp ähnelt mehreren OLE-Typen wie VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Signierte oder nicht signierte 64-Bit-Ganzzahl (8 Byte), die die **LARGE_INTEGER** -Struktur verwendet. Dieser Eigenschaftentyp ist identisch mit PT_I8 und dem OLE-Typ VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |NULL-terminierte 8-Bit-Zeichenfolge (2 Byte). Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Mit NULL abgeschlossene 16-Bit-Zeichenfolge (2 Byte). Eigenschaften mit diesem Typ haben den Eigenschaftentyp auf PT_UNICODE zurückgesetzt, wenn Sie mit dem UNICODE-Symbol kompiliert werden, und zu PT_STRING8, wenn Sie nicht mit dem UNICODE-Symbol kompiliert werden. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_LPSTR für die resultierenden PT_STRING8-Eigenschaften und VT_LPWSTR für PT_UNICODE-Eigenschaften  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64-Bit-Ganzzahl (8 Byte)-Daten und Zeitwert in Form einer FILETIME **** -Struktur. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID** -Struktur Wert. Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Variable Größe, eine 16-Bit- **Anzahl** (2 Byte), gefolgt von einer Struktur.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Variable Größe, ein Bytearray, das eine oder mehrere Einschränkungs Strukturen darstellt.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Variable Größe, eine 16-Bit- **Anzahl** (2 Byte) von Aktionen (nicht Byte), gefolgt von den vielen Regel Aktions Strukturen.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary** -Struktur Wert, ein Gezähltes Bytearray.  <br/> |
   
> [!NOTE]
> Um den Hex-Wert für den mehrwertigen Eigenschaftentyp oder das PT_MV-Flag (0x00001000) für den Eigenschaftentyp zu bestimmen. Beispielsweise ist der Hex-Wert für PT_MV_UNICODE 0x101F, und der Hex-Wert für PT_MV_BINARY ist 0x1102. 
  


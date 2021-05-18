---
title: Eigenschaftstypen
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
# <a name="property-types"></a>Eigenschaftstypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI unterstützt sowohl Ein-Wert- als auch Mehrere-Wert-Eigenschaften. Bei einer Ein-Wert-Eigenschaft gibt es einen Wert des Basistyps für die Eigenschaft. Bei einer Eigenschaft mit mehreren Werten gibt es mehrere Werte des Basistyps. 
  
Die von MAPI unterstützten Eigenschaftstypen mit einem wert- und mehreren Wert werden in der folgenden Tabelle beschrieben. Für jeden einzelnen Werttyp, der einen entsprechenden Mehrwerttyp besitzt, wird der Typ mit mehreren Wert in Klammern nach dem Ein-Wert-Typ angezeigt.
  
|**Eigenschaftstyp**|**Hex-Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Gibt an, dass der Eigenschaftentyp unbekannt ist. Dieser Eigenschaftstyp ist für die Verwendung mit Schnittstellenmethoden reserviert.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Gibt keinen Eigenschaftswert an. Dieser Eigenschaftstyp ist für die Verwendung mit Schnittstellenmethoden reserviert und identisch mit dem OLE-VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Signierte 16-Bit-Ganzzahl (2 Byte). Dieser Eigenschaftstyp ist identisch mit PT_SHORT (PT_MV_SHORT) und dem OLE-Typ VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Signierte oder nicht signierte 32-Bit-Ganzzahl (4 Byte). Dieser Eigenschaftstyp ist identisch mit PT_LONG (PT_MV_LONG) und dem OLE-Typ VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32-Bit-Gleitkommawert (8 Byte). Dieser Eigenschaftstyp ist identisch mit PT_R4 (PT_MV_R4) und dem OLE-Typ VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64-Bit-Gleitkommawert (8 Byte). Dieser Eigenschaftstyp ist identisch mit PT_R8 und den OLE-Typen VT_R8 und VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY )  <br/> |0006  <br/> |64-Bit-Ganzzahl (8 Byte), die als Dezimalzahl interpretiert wird. Dieser Eigenschaftentyp ist mit dem Microsoft Visual Basic CURRENCY-Typ kompatibel und identisch mit dem OLE-Typ VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Double-Wert, der als Datum und Uhrzeit interpretiert wird. Der ganzzahligen Teil ist das Datum und das zu rundende Teil ist die Zeit. Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_DATE und ist mit der Microsoft Visual Basic kompatibel.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE-Wert; 32-Bit-Ganzzahl (4 Byte) ohne Vorzeichen. Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000 B  <br/> |Boolescher 16-Bit-Wert (2 Byte), wobei Null gleich **false** und nicht Null true **ist.** Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Zeiger auf ein Objekt, das die **IUnknown-Schnittstelle** implementiert. Dieser Eigenschaftstyp ähnelt mehreren OLE-Typen, z. B. VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Signierte oder nicht signierte 64-Bit-Ganzzahl (8 Byte), die die LARGE_INTEGER verwendet.  Dieser Eigenschaftstyp ist identisch mit PT_I8 und dem OLE-Typ VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Null-terminated 8-bit (2-byte) character string. Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Null-terminated 16-Bit (2-Byte)-Zeichenzeichenfolge. Eigenschaften mit diesem Typ setzen den Eigenschaftstyp auf PT_UNICODE beim Kompilieren mit dem UNICODE-Symbol und PT_STRING8, wenn sie nicht mit dem UNICODE-Symbol kompiliert werden. Dieser Eigenschaftstyp ist identisch mit dem OLE-Typ VT_LPSTR für resultierende PT_STRING8 und VT_LPWSTR für PT_UNICODE Eigenschaften.  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64-Bit(8-Byte)-ganzzahlige Daten und Zeitwerte in Form einer **FILETIME-Struktur.** Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID-Strukturwert.** Dieser Eigenschaftstyp ist identisch mit dem OLE-VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Variable Größe, eine 16-Bit-COUNT (2 Byte), gefolgt von einer Struktur.   <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Variable Größe, ein Bytearray, das eine oder mehrere Einschränkungsstrukturen darstellt.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Variable Größe, eine 16-Bit-ANZAHL (2 **Byte)** von Aktionen (nicht Byte), gefolgt von vielen Regelaktionsstrukturen.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary-Strukturwert,** ein gezähltes Bytearray.  <br/> |
   
> [!NOTE]
> Um den Hex-Wert für den mehrwertigen Eigenschaftstyp zu bestimmen, oder das PT_MV (0x00001000) auf den Hex-Wert für den Eigenschaftentyp. Beispielsweise ist der Hex-Wert für PT_MV_UNICODE 0x101F und der Hex-Wert für PT_MV_BINARY 0x1102. 
  


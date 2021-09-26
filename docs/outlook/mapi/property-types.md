---
title: Eigenschaftstypen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d211426240d5bee73c1afb59d8905fefa727e6fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624391"
---
# <a name="property-types"></a>Eigenschaftstypen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI unterstützt sowohl Einwert- als auch Mehrfachwerteigenschaften. Bei einer einwertigen Eigenschaft gibt es einen Wert des Basistyps für die Eigenschaft. Bei einer Eigenschaft mit mehreren Werten gibt es mehrere Werte des Basistyps. 
  
Die von mapi unterstützten Eigenschaftentypen mit einem wertigen und mehreren Werten werden in der folgenden Tabelle beschrieben. Für jeden einwertigen Typ, der einen entsprechenden Mehrfachwerttyp aufweist, wird der Mehrfachwerttyp in Klammern hinter dem Einwerttyp angezeigt.
  
|**Eigenschaftstyp**|**Hex-Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Gibt an, dass der Eigenschaftentyp unbekannt ist. Dieser Eigenschaftstyp ist für die Verwendung mit Schnittstellenmethoden reserviert.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Gibt keinen Eigenschaftswert an. Dieser Eigenschaftstyp ist für die Verwendung mit Schnittstellenmethoden reserviert und entspricht dem OLE-Typ VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |16-Bit-Ganzzahl mit Vorzeichen (2 Byte). Dieser Eigenschaftentyp ist identisch mit PT_SHORT (PT_MV_SHORT) und dem OLE-Typ VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |32-Bit-Ganzzahl mit Vorzeichen oder ohne Vorzeichen (4 Byte). Dieser Eigenschaftentyp ist identisch mit PT_LONG (PT_MV_LONG) und dem OLE-Typ VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32-Bit-Gleitkommawert (8 Byte). Dieser Eigenschaftentyp ist identisch mit PT_R4 (PT_MV_R4) und dem OLE-Typ VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64-Bit-Gleitkommawert (8 Byte). Dieser Eigenschaftstyp entspricht PT_R8 und den OLE-Typen VT_R8 und VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY )  <br/> |0006  <br/> |64-Bit-Ganzzahl (8 Byte), die als Dezimalzahl interpretiert wird. Dieser Eigenschaftentyp ist kompatibel mit dem Currency-Typ von Microsoft Visual Basic und entspricht dem OLE-Typ VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Doppelter Wert, der als Datum und Uhrzeit interpretiert wird. Der ganzzahligen Teil ist das Datum und das zu rundende Teil ist die Zeit. Dieser Eigenschaftstyp ist mit dem OLE-Typ VT_DATE identisch und mit der Zeitdarstellung von Microsoft Visual Basic kompatibel.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE-Wert; 32-Bit-Ganzzahl ohne Vorzeichen (4 Byte). Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16-Bit-Wert (2-Byte) Boolescher Wert, wobei Null **"false"** und "nicht Null" **"true"** entspricht. Dieser Eigenschaftstyp ist identisch mit dem OLE-Typ VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Zeiger auf ein Objekt, das die **IUnknown-Schnittstelle** implementiert. Dieser Eigenschaftstyp ähnelt mehreren OLE-Typen, z. B. VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Vorzeichen- oder nicht signierte 64-Bit-Ganzzahl (8-Byte), die die **LARGE_INTEGER-Struktur** verwendet. Dieser Eigenschaftentyp ist identisch mit PT_I8 und dem OLE-Typ VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Mit Null beendete 8-Bit-Zeichenfolge (2-Byte). Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Mit Null terminierte 16-Bit-Zeichenfolge (2-Byte). Eigenschaften mit diesem Typ werden beim Kompilieren mit dem UNICODE-Symbol auf PT_UNICODE zurückgesetzt und beim Kompilieren mit dem UNICODE-Symbol auf PT_STRING8, wenn sie nicht mit dem UNICODE-Symbol kompiliert werden. Dieser Eigenschaftstyp ist identisch mit dem OLE-Typ VT_LPSTR für resultierende PT_STRING8 Eigenschaften und VT_LPWSTR für PT_UNICODE Eigenschaften  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64-Bit-Ganzzahldaten (8 Byte) und Zeitwert in Form einer **FILETIME-Struktur.** Dieser Eigenschaftstyp ist identisch mit dem OLE-Typ VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**CLSID-Strukturwert.** Dieser Eigenschaftentyp ist identisch mit dem OLE-Typ VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Variable Größe, 16-Bit(2-Byte)-ANZAHL gefolgt von einer Struktur.   <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Variable Größe, ein Bytearray, das eine oder mehrere Einschränkungsstrukturen darstellt.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Variable Größe, eine 16-Bit (2-Byte)-ANZAHL von Aktionen (nicht Byte), gefolgt von dieser Anzahl von Regelaktionsstrukturen.   <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary-Strukturwert,** ein gezähltes Bytearray.  <br/> |
   
> [!NOTE]
> Um den Hexadezimalwert für den mehrwertigen Eigenschaftstyp zu bestimmen, ODER das PT_MV Flag (0x00001000) zum Hex-Wert für den Eigenschaftstyp. For example, the Hex value for PT_MV_UNICODE is 0x101F and the Hex value for PT_MV_BINARY is 0x1102. 
  


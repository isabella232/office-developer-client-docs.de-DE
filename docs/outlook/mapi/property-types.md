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
ms.openlocfilehash: fba09af82a3eccc05c72e44ffea14ca979714ff0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563597"
---
# <a name="property-types"></a>Eigenschaftentypen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI unterstützt einwertig und mehrwertige Eigenschaften. Mit einer einwertigen-Eigenschaft ist ein Wert, der den Basistyp für die Eigenschaft vorhanden. Eine mehrwertige Eigenschaft sind mehrere Werte des Basistyps. 
  
Die einwertig und mehrwertige Eigenschaften aufgeführt, die MAPI unterstützt werden in der folgenden Tabelle beschrieben. Für jede Art von Single-Wert mit dem entsprechenden mehrwertige Typ die mehrwertige Art angezeigt in Klammern nach dem Typ Single-Wert.
  
|**Eigenschaftstyp**|**Hex-Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Gibt an, dass es sich bei der Typ unbekannt ist. In diesem Eigenschaftentyp ist für die Verwendung mit Schnittstellenmethoden reserviert.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Gibt keinen Eigenschaftswert an. In diesem Eigenschaftentyp ist für die Verwendung mit Schnittstellenmethoden reserviert und handelt es sich um die gleiche wie die OLE VT_NULL geben.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |16-Bit (2-Byte) ganze Zahl mit Vorzeichen. In diesem Eigenschaftentyp entspricht dem PT_SHORT (PT_MV_SHORT) und das OLE-VT_I2 eingeben.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |(Mit oder ohne Vorzeichen 32-Bit 4-Byte), ganze Zahl. In diesem Eigenschaftentyp entspricht dem PT_LONG (PT_MV_LONG) und das OLE-VT_I4 eingeben.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |32-Bit (8-Byte) Gleitkommawert. In diesem Eigenschaftentyp entspricht dem PT_R4 (PT_MV_R4) und den OLE-Typ VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |64-Bit (8-Byte) Gleitkommawert. In diesem Eigenschaftentyp entspricht dem PT_R8 und der OLE-Typen VT_R8 und VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64-Bit (8-Byte), ganze Zahl, die als Dezimalzahl interpretiert werden. In diesem Eigenschaftentyp ist kompatibel mit dem Microsoft Visual Basic-Währungstyp und handelt es sich um die gleiche wie die OLE VT_CY geben.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Double-Wert, der als Datum und Uhrzeit interpretiert wird. Der ganzzahligen Teil ist das Datum und das zu rundende Teil ist die Zeit. Diesem Eigenschaftentyp ist identisch mit dem OLE-Typ VT_DATE und mit der Microsoft Visual Basic-zeitdarstellung kompatibel ist.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |SCODE-Wert. 32-Bit-Ganzzahl (4-Byte) ohne Vorzeichen. In diesem Eigenschaftentyp entspricht dem OLE-Typ VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000 B  <br/> |16-Bit (2-Byte) boolescher Wert, auf dem gleich null **false** und ungleich NULL ist gleich **true**ist. In diesem Eigenschaftentyp entspricht dem OLE-Typ VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Zeiger auf ein Objekt, das die **IUnknown** -Schnittstelle implementiert wird. Mehrere OLE-Typen wie VT_UNKNOWN ähnelt diesem Eigenschaftentyp.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Mit oder ohne Vorzeichen 64-Bit (8-Byte) ganze Zahl, die die Struktur **LARGE_INTEGER** verwendet. In diesem Eigenschaftentyp entspricht dem PT_I8 und das OLE-VT_I8 eingeben.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |NULL 8-Bit (2-Byte) endende Zeichenfolge. In diesem Eigenschaftentyp entspricht dem OLE-Typ VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |NULL 16-Bit (2-Byte) endende Zeichenfolge. Eigenschaften mit diesem Typ haben den Eigenschaftentyp zurücksetzen PT_UNICODE beim Kompilieren mit dem UNICODE-Zeichen und PT_STRING8 beim Kompilieren von nicht mit dem UNICODE-Zeichen. In diesem Eigenschaftentyp ist identisch mit den OLE-Typ VT_LPSTR für resultierende PT_STRING8 Eigenschaften und VT_LPWSTR für PT_UNICODE-Eigenschaften  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |64-Bit (8-Byte) Datum und Uhrzeit Ganzzahlwert in Form von eine **FILETIME** -Struktur. In diesem Eigenschaftentyp entspricht dem OLE-Typ VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Struktur **CLSID** -Wert. In diesem Eigenschaftentyp entspricht dem OLE-Typ VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Variable Größe einer 16-Bit (2-Byte) **Anzahl** gefolgt von einer Struktur.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Variabler Größe, die ein Byte-Array, das eine oder mehrere Einschränkung Strukturen darstellt.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Variable Größe gefolgt eine 16-Bit (2-Byte) **Anzahl** der Aktionen (nicht Bytes), die viele Regelaktion Strukturen.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**SBinary** Struktur Wert gezählte Bytearray zurück.  <br/> |
   
> [!NOTE]
> Geben den Hex-Wert für den Typ mehrwertige Eigenschaft oder die PT_MV bestimmen Flag (0 x 00001000) auf den Hex-Wert für die Eigenschaft ein. Beispiel der Hex-Wert für PT_MV_UNICODE ist 0x101F und der Hex-Wert für PT_MV_BINARY ist 0 x 1102. 
  


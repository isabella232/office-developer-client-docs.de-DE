---
title: FORMATEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797069"
---
# <a name="formatex-function"></a>FORMATEX Function

Gibt das Ergebnis von Expression in SrcUnit als Zeichenfolge ausgewertet formatiert entsprechend Format wurde.
  
## <a name="syntax"></a>Syntax

FORMATEX (** *Ausdruck* **, "** *Format* **", [** *SrcUnit* **], [** *DstUnit* **], [** *LangID* **] [, ** *CalID* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Formatierungsangabe zum Formatieren der Zeichenfolge verwendet. Weitere Informationen zu Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).  <br/> |
| _srcUnit_ <br/> |Optional  <br/> |**String** <br/> | Einheiten zum Auswerten von expression (in, cm usw.).  <br/> |
| _dstUnit_ <br/> |Optional  <br/> |**String** <br/> |Einheiten, die für das Ergebnis von expression verwendet werden sollen (in, cm usw.).  <br/> |
| _langID_ <br/> |Optional  <br/> |**Nummer** <br/> |Die Sprache, die beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
| _calID_ <br/> |Optional  <br/> |**Nummer** <br/> |Der Kalender, der beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. format muss für den Typ des Ausdrucks gültig sein.
  
Mit dem srcUnit-Argument werden typenlose Ergebnisse eines Ausdrucks skaliert, z. B. 3 + 4. Wenn das Ergebnis von expression ausdrücklich einen Typ besitzt, z. B. 3 cm + 8 cm, wird srcUnit ignoriert.
  
Mit dem dstUnit-Argument werden die Maßeinheiten für das formatierte Ergebnis bestimmt. Wenn dstUnit nicht angegeben wurde, werden die Einheiten für das Ergebnis des Ausdrucks verwendet.
  
Ein Fehler wird zurückgegeben, wenn das Ergebnis von expression und der erwartete Typ in format unterschiedlich sind, wenn in format Syntaxfehler enthalten sind oder die als srcUnit bzw. dstUnit übergebenen Einheiten nicht erkannt werden.
  
## <a name="example"></a>Beispiel

FORMATEX(5.5, "0,00 u", "cm", "ft") 
  
Gibt 0,18 Fuß zurück. 
  


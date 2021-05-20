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
description: Gibt das Ergebnis des In srcUnit ausgewerteten Ausdrucks als Zeichenfolge zurück, die gemäß dem in dstUnit ausgedrückten Format formatiert ist.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430966"
---
# <a name="formatex-function"></a>FORMATEX Function

Gibt das Ergebnis des In srcUnit ausgewerteten Ausdrucks als Zeichenfolge zurück, die gemäß dem in dstUnit ausgedrückten Format formatiert ist.
  
## <a name="syntax"></a>Syntax

FORMATEX(** *Expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
| _format_ <br/> |Erforderlich  <br/> |**String** <br/> |Das Formatbild, das zum Formatieren der Zeichenfolge verwendet wird. Weitere Informationen zum Formatieren von Bildern finden Sie unter [About Format Pictures](about-format-pictures.md).  <br/> |
| _srcUnit_ <br/> |Optional  <br/> |**String** <br/> | Einheiten zum Auswerten von expression (in, cm usw.).  <br/> |
| _dstUnit_ <br/> |Optional  <br/> |**String** <br/> |Einheiten, die für das Ergebnis von expression verwendet werden sollen (in, cm usw.).  <br/> |
| _langID_ <br/> |Optional.  <br/> |**Number** <br/> |Die Sprache, die beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
| _calID_ <br/> |Optional.  <br/> |**Number** <br/> |Der Kalender, der beim Formatieren von Datums-/Zeitangaben in Microsoft Office System verwendet wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge. format muss für den Typ des Ausdrucks gültig sein.
  
Mit dem srcUnit-Argument werden typenlose Ergebnisse eines Ausdrucks skaliert, z. B. 3 + 4. Wenn das Ergebnis von expression ausdrücklich einen Typ besitzt, z. B. 3 cm + 8 cm, wird srcUnit ignoriert.
  
Mit dem dstUnit-Argument werden die Maßeinheiten für das formatierte Ergebnis bestimmt. Wenn dstUnit nicht angegeben wurde, werden die Einheiten für das Ergebnis des Ausdrucks verwendet.
  
Ein Fehler wird zurückgegeben, wenn das Ergebnis von expression und der erwartete Typ in format unterschiedlich sind, wenn in format Syntaxfehler enthalten sind oder die als srcUnit bzw. dstUnit übergebenen Einheiten nicht erkannt werden.
  
## <a name="example"></a>Beispiel

FORMATEX(5.5, "0,00 u", "cm", "ft") 
  
Gibt 0,18 Fuß zurück. 
  


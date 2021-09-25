---
title: SHAPETEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
ms.localizationpriority: medium
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Ruft den Text aus einer Form ab.
ms.openlocfilehash: bfd33bb6fe0aca144372474e484e31f095715e0d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622893"
---
# <a name="shapetext-function"></a>SHAPETEXT Function

Ruft den Text aus einer Form ab. 
  
## <a name="syntax"></a>Syntax

SHAPETEXT (** *Shapename! TheText* ** ** *[,flag]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! TheText_ <br/> |Erforderlich  <br/> ||Ein Verweis auf die Zelle mit dem Namen "TheText" im Ziel-Shape.  _Shapename!_ ist der Name des Shapes, aus dem der Text abgerufen werden soll.  <br/> |
| _Flag_ <br/> |Optional  <br/> |**Numeric** <br/> |Ein Bit, das das Format des Texts bestimmt. Wenn das Standard-Flag (0) verwendet wird, wird der Text genauso wie im Shape dargestellt.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Sie können eine beliebige Kombination folgender Flags mit der Funktion SHAPETEXT verwenden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Zeigt den Text genau wie in dem Shape an.  <br/> |
|1  <br/> |Willkürliche Bindestriche einschließen.  <br/> |
|2  <br/> |Keinen erweiterten Text in Feldern einschließen.  <br/> |
|4   <br/> |Tabulatorzeichen in ein einzelnes Leerzeichen konvertieren.  <br/> |
|8   <br/> |Tabulatorzeichen in mehrere Leerzeichen konvertieren.  <br/> |
|16   <br/> |Zeilenschaltungen und Zeilenumbrüche in Leerzeichen konvertieren.  <br/> |
|32  <br/> |Typografische Anführungszeichen in normale Anführungszeichen konvertieren.  <br/> |
|64  <br/> |Benachbarte Leerzeichen in ein einzelnes Leerzeichen konvertieren.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

SHAPETEXT(sheetN!theText)
  
Gibt den Text aus dem Shape namens sheetN genau so zurück, wie er in dem Shape angezeigt ist.
  
## <a name="example-2"></a>Beispiel 2

SHAPETEXT(theText)
  
Gibt den Text aus dem aktuellen Shape genau so zurück, wie er in dem Shape angezeigt ist.
  
## <a name="example-3"></a>Beispiel 3

SHAPETEXT(DerText, 84)
  
Gibt den Text des aktuellen Shapes zurück. Außerdem werden benachbarte Leerzeichen in ein einzelnes Leerzeichen (64), Zeilenschaltungen und Zeilenumbrüche (16) in Leerzeichen und Tabulatoren in ein einzelnes Leerzeichen konvertiert. Die Summe dieser Flags ist 84.
  


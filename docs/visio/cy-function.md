---
title: CY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Gibt einen Währungswert zurück.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796759"
---
# <a name="cy-function"></a>CY Function

Gibt einen Währungswert zurück.
  
## <a name="syntax"></a>Syntax

CY (** *Wert* **, ** *CyID* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Value_ <br/> |Optional  <br/> |**Zahl oder eine Zeichenfolge** <br/> |Eine Zahl oder eine Zeichenfolge, die Währung-spezifischen Formatierung enthält. Wenn nicht angegeben, wird der Währungswert entsprechend das Währungsformat in die Standardeinstellungen des Systems Region und Sprache formatiert.  <br/> |
| _cyID_ <br/> |Optional  <br/> |**Nummer** <br/> |Eine numerische Währung-ID oder eine Zeichenfolge mit drei Zeichen in Anführungszeichen für die Abkürzung ISO 4217.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine andere Währung angeben, müssen Sie eine gültige _CyID_einbeziehen. Eine Liste finden Sie unter [About Currency-Konstanten](about-currency-constants.md).
  
Wenn der _Wert_ nicht kompatibel mit dem angegebenen Währungstyp ist oder wenn ein ungültiges Argument wie "keine Zahl" angegeben ist, wird ein #VALUE! Fehler wird zurückgegeben. Wenn der _Wert größer als 922,337,203,685,477.5807 oder kleiner als -922.337.203.685.477,5808 ist, wird ein #VALUE!_ Fehler wird zurückgegeben. 
  
Verwenden Sie für eine bessere Genauigkeit mit sehr großen Währungswerten mit Bruchzahlangaben für eine Einheit wie 3.6 Billionen, Zeichenfolge-Argumente _Wert_.
  
Angabe einer ungültigen _CyID_ wird ein Fehler zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

Wenn der Benutzer in den Regions- und Spracheinstellungen US-Dollar festgelegt hat:
  
CY(999998.993)
  
Gibt $999.998,99 zurück.
  
## <a name="example-2"></a>Beispiel 2

CY(12345678,993. "USD")
  
Gibt $12.345.678,99 zurück.
  
## <a name="example-3"></a>Beispiel 3

CY(12345678,993. "EUR")
  
Gibt 12.345.678,99 € zurück.
  
## <a name="example-4"></a>Beispiel 4

CY(12345678,7832. "XXX")
  
Gibt 12.345.678,78 zurück.
  


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
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433556"
---
# <a name="cy-function"></a>CY Function

Gibt einen Währungswert zurück.
  
## <a name="syntax"></a>Syntax

CY(** *value* **, ** *cyID* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Optional.  <br/> |**Nummer oder Zeichenfolge** <br/> |Eine Zahl oder eine Zeichenfolge, die währungsspezifische Formatierungen enthält. Wenn dieser Wert nicht angegeben wird, wird der Währungswert gemäß der Währungsformatvorlage in den Einstellungen Region und Sprache des Systems formatiert.  <br/> |
| _cyID_ <br/> |Optional.  <br/> |**Number** <br/> |Eine numerische Währungs-ID oder eine zeichenfolge mit drei Zeichen für die ISO 4217-Abkürzung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine andere Währung anzugeben, müssen Sie eine gültige _cyID angeben._ Eine entsprechende Liste finden Sie unter [Informationen zu Währungskonstanten](about-currency-constants.md).
  
Wenn  _der Wert_ mit dem angegebenen Währungstyp nicht kompatibel ist oder wenn ein ungültiges Argument wie "keine Zahl" angegeben wird, wird #VALUE! zurückgegeben. Wenn  _der_ Wert größer als 922.337.203.685.477,5807 oder kleiner als -922.337.203.685.477,5808 ist, ist #VALUE! zurückgegeben. 
  
Für eine bessere Genauigkeit bei sehr großen Währungswerten, die Bruchteile einer Einheit enthalten, z. B. 3,6 Billionen, verwenden Sie Zeichenfolgenargumente für  _den Wert_.
  
Das Angeben einer ungültigen  _cyID_ gibt einen Fehler zurück. 
  
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
  


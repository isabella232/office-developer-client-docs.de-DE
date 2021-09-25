---
title: CY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
ms.localizationpriority: medium
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Gibt einen Währungswert zurück.
ms.openlocfilehash: a94be94db24d9e9f34acf7289878295d4b35c66d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594664"
---
# <a name="cy-function"></a>CY Function

Gibt einen Währungswert zurück.
  
## <a name="syntax"></a>Syntax

CY(**-Wert **, ** *cyID* ** )  
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Optional  <br/> |**Nummer oder Zeichenfolge** <br/> |Eine Zahl oder eine Zeichenfolge, die währungsspezifische Formatierung enthält. Wenn nicht angegeben, wird der Währungswert gemäß der Währungsformatvorlage in den Regions- und Spracheinstellungen des Systems formatiert.  <br/> |
| _cyID_ <br/> |Optional  <br/> |**Number** <br/> |Eine numerische Währungs-ID oder eine aus drei Zeichen bestehende Zeichenfolge für die ISO 4217-Abkürzung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um eine andere Währung anzugeben, müssen Sie eine gültige  _cyID_ angeben. Eine entsprechende Liste finden Sie unter [Informationen zu Währungskonstanten](about-currency-constants.md).
  
Wenn  _der Wert_ mit dem angegebenen Währungstyp nicht kompatibel ist oder wenn ein ungültiges Argument wie "keine Zahl" angegeben wird, #VALUE! zurückgegeben. Wenn  _der Wert_ größer als 922.337.203.685.477.5807 oder kleiner als -922.337.203.685.477,5808 ist, #VALUE! zurückgegeben. 
  
Verwenden Sie für eine bessere Genauigkeit bei sehr großen Währungswerten, die Bruchteile einer Einheit enthalten, z. B. 3,6 Billionen, Zeichenfolgenargumente für _den Wert._
  
Wenn Sie eine  _ungültige CyID angeben,_ wird ein Fehler zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

Wenn der Benutzer in den Regions- und Spracheinstellungen US-Dollar festgelegt hat:
  
CY(999998,993)
  
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
  


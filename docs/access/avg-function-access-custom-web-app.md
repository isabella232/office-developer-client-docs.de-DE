---
title: Avg-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel eines Wertesatzs, der in einem angegebenen Feld enthalten ist.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426723"
---
# <a name="avg-function-access-custom-web-app"></a>Avg-Funktion (benutzerdefinierte Access-Web-App)

Berechnet das arithmetische Mittel eines Wertesatzs, der in einem angegebenen Feld enthalten ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Avg** (*NumericExpression*) 
  
Die **Avg-Funktion** enthält das folgende Argument. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|NumericExpression  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Sie durchschnittlich verwenden möchten, oder ein Ausdruck, der eine Berechnung mit den Daten in diesem Feld durchführt. Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Variablen oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine der anderen Aggregatfunktionen SQL kann).  <br/> |
   
## <a name="remarks"></a>Hinweise

Bei dem von der **Avg**-Funktion berechneten Durchschnittswert handelt es sich um das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl von Werten). Mithilfe der **Avg**-Funktion können Sie beispielsweise die durchschnittlichen Frachtkosten berechnen. 
  
Die **Avg-Funktion** enthält keine **Null-Werte** in der Berechnung. 
  


---
title: AVG-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel einer Gruppe von Werten, die in einem angegebenen Feld enthalten sind.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282334"
---
# <a name="avg-function-access-custom-web-app"></a>AVG-Funktion (Access Custom Web App)

Berechnet das arithmetische Mittel einer Gruppe von Werten, die in einem angegebenen Feld enthalten sind.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **AVG** (*Numerischer Ausdruck*) 
  
Die **AVG** -Funktion enthält das folgende Argument. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|Numerischer Ausdruck  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Sie durchsuchen möchten, oder einen Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld ausführt. Operanden in *numericive* können den Namen eines Tabellenfelds, einer Variablen oder einer Funktion enthalten (Dies kann entweder systeminterne oder benutzerdefinierte, aber nicht eine der anderen SQL-Aggregatfunktionen sein).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei dem von der **Avg**-Funktion berechneten Durchschnittswert handelt es sich um das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl von Werten). Mithilfe der **Avg**-Funktion können Sie beispielsweise die durchschnittlichen Frachtkosten berechnen. 
  
Die **AVG** -Funktion enthält keine **null** -Werte in der Berechnung. 
  


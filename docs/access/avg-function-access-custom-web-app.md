---
title: Avg-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel einer Gruppe von Werten, die in einem angegebenen Feld enthalten sind.
ms.openlocfilehash: 7b05417328aac255197bba55726a835e58e36fff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562895"
---
# <a name="avg-function-access-custom-web-app"></a>Avg-Funktion (benutzerdefinierte Access-Web-App)

Berechnet das arithmetische Mittel einer Gruppe von Werten, die in einem angegebenen Feld enthalten sind.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Avg** (*NumericExpression*) 
  
Die **Avg-Funktion** enthält das folgende Argument. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|NumericExpression  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Sie durchschnittlich verwenden möchten, oder ein Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld durchführt. Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Variablen oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte Funktionen sein kann, jedoch keine der anderen SQL Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Bei dem von der **Avg**-Funktion berechneten Durchschnittswert handelt es sich um das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl von Werten). Mithilfe der **Avg**-Funktion können Sie beispielsweise die durchschnittlichen Frachtkosten berechnen. 
  
Die **Avg-Funktion** enthält keine **Nullwerte** in der Berechnung. 
  


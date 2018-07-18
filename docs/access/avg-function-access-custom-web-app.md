---
title: AVG-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Berechnet das arithmetische Mittel einer Gruppe von Werten zurück, die in einem angegebenen Feld enthalten sind.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790192"
---
# <a name="avg-function-access-custom-web-app"></a>AVG-Funktion (Access benutzerdefinierte Web app)

Berechnet das arithmetische Mittel einer Gruppe von Werten zurück, die in einem angegebenen Feld enthalten sind.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **AVG** (*NumericExpression*) 
  
Die **Avg** -Funktion enthält das folgende Argument. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|NumericExpression  <br/> |Ein Zeichenfolgenausdruck, der das Feld mit den numerischen Daten möchten Sie Mittelwert oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird. Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Variable oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei dem von der **Avg**-Funktion berechneten Durchschnittswert handelt es sich um das arithmetische Mittel (die Summe der Werte dividiert durch die Anzahl von Werten). Mithilfe der **Avg**-Funktion können Sie beispielsweise die durchschnittlichen Frachtkosten berechnen. 
  
Die **Avg** -Funktion umfasst keine **Null** -Werte in der Berechnung. 
  


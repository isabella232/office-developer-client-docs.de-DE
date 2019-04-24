---
title: Count-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282236"
---
# <a name="count-function-access-custom-web-app"></a>Count-Funktion (Access Custom Web App)

Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Anzahl** (*Ausdruck*) 
  
Die **count** -Funktion enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Ausdruck*  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die zu zählenden Daten enthält, oder ein Ausdruck, der eine Berechnung mithilfe der Daten im Feld ausführt. Operanden in *Expression* können den Namen eines Tabellenfelds oder einer Funktion enthalten (Dies kann sowohl systeminterne als auch benutzerdefinierte, aber nicht andere SQL-Aggregatfunktionen sein). Sie können beliebige Daten, einschließlich Text, zählen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mithilfe der Count-Funktion kann die Anzahl von Datensätzen in einer zugrunde liegenden Abfrage gezählt werden. Sie können beispielsweise count verwenden, um die Anzahl der Bestellungen zu ermitteln, die an ein bestimmtes Land oder eine bestimmte Region geliefert wurden.
  
**Anzahl** (\*) gibt die Anzahl der Elemente in einer Gruppe zurück. Dazu gehören NULL-Werte und Duplikate. 
  


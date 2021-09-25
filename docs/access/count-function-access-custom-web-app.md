---
title: Count-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl der Datensätze in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 5eb0bb9f97184a5250b19d5c291d97a029005ab1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577682"
---
# <a name="count-function-access-custom-web-app"></a>Count-Funktion (benutzerdefinierte Access-Web-App)

Gibt die Anzahl der Datensätze in einer Abfrage oder Tabelle zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Count** (*Ausdruck*) 
  
Die **Count-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Ausdruck*  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die zu zählenden Daten enthält, oder ein Ausdruck, der eine Berechnung mithilfe der Daten im Feld durchführt. Operanden in *Ausdruck* können den Namen eines Tabellenfelds oder einer Tabellenfunktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine anderen SQL Aggregatfunktionen sein können). Sie können beliebige Daten, einschließlich Text, zählen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe der Count-Funktion kann die Anzahl von Datensätzen in einer zugrunde liegenden Abfrage gezählt werden. Sie können beispielsweise Count verwenden, um die Anzahl der Bestellungen zu zählen, die in ein bestimmtes Land oder eine bestimmte Region versandt wurden.
  
**Count** ( \* ) gibt die Anzahl der Elemente in einer Gruppe zurück. Dies schließt NULL-Werte und Duplikate ein. 
  


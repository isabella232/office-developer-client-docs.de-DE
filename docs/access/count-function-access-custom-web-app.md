---
title: Count-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790212"
---
# <a name="count-function-access-custom-web-app"></a>Count-Funktion (Access benutzerdefinierte Web app)

Gibt die Anzahl von Datensätzen in einer Abfrage oder Tabelle zurück.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Count** (*Ausdruck*) 
  
Die **Count** -Funktion enthält das folgende Argument. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Ein Zeichenfolgenausdruck, der das Feld, das Daten enthält, die Sie Count oder ein Ausdruck, der eine Berechnung mit den Daten in das Feld durchführt möchten. Zu den Operanden von *Ausdruck* zählen der Name des Felds oder Funktion (die integrierte oder benutzerdefinierte werden können, jedoch keine anderen SQL-Aggregatfunktionen). Sie können jede Art von Daten, einschließlich Text zählen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Count können Sie die Anzahl der Datensätze in einer zugrunde liegenden Abfrage zählen. Count können Sie beispielsweise die Anzahl von Bestellungen, die einem bestimmten Land oder einer Region zählen.
  
**Count** (\*) die Anzahl der Elemente in einer Gruppe zurückgegeben. Dazu gehören NULL-Werte und Duplikate. 
  


---
title: Count-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Gibt die Anzahl der Datensätze in einer Abfrage oder Tabelle zurück.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419142"
---
# <a name="count-function-access-custom-web-app"></a>Count-Funktion (benutzerdefinierte Access-Web-App)

Gibt die Anzahl der Datensätze in einer Abfrage oder Tabelle zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Count** (*Expression*) 
  
Die **Count-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Ausdruck*  <br/> |Ein Zeichenfolgenausdruck, der das Feld identifiziert, das die daten enthält, die Sie zählen möchten, oder ein Ausdruck, der eine Berechnung mit den Daten im Feld ausführt. Operanden in *Expression* können den Namen eines Tabellenfelds oder einer -funktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine anderen SQL sein können). Sie können beliebige Daten, einschließlich Text, zählen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Mithilfe der Count-Funktion kann die Anzahl von Datensätzen in einer zugrunde liegenden Abfrage gezählt werden. Sie können beispielsweise Count verwenden, um die Anzahl der Bestellungen zu zählen, die in ein bestimmtes Land oder eine bestimmte Region versandt wurden.
  
**Count** ( \* ) gibt die Anzahl der Elemente in einer Gruppe zurück. Dies umfasst NULL-Werte und Duplikate. 
  


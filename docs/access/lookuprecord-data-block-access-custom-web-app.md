---
title: NachschlagenDatensatz-Datenblock (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.
ms.openlocfilehash: 76020c4afc9188a432f78fd78bed56aa8096e67c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605792"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>NachschlagenDatensatz-Datenblock (benutzerdefinierte Access-Web-App)

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _In_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll. Das Argument *"In"* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL Anweisung enthalten.  <br/> |
| _Bedingung_ <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der zum Einschränken des Datenbereichs verwendet wird, für den der **Nachschlagedatenblock** ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der **Datenblock "LookupRecord"** für die gesamte durch das Argument  *"In"*  angegebene Domäne ausgeführt. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in  *In*  sein.  <br/> |
| _Alias_ <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für den durch das  *Argument "In"*  angegebenen Datensatz bereitstellt. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn  *alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt. 
  
Wenn kein Datensatz  *"Where Condition"*  erfüllt oder wenn  *"In"*  keine Datensätze enthält, erstellt **LookupRecord** einen leeren Datensatz, in dem alle Felder einen **Null-Wert** enthalten. 
  


---
title: NachschlagenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790237"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>NachschlagenDatensatz-Datenblock (Access benutzerdefinierte Web app)

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> [!HINWEIS] Der **NachschlagenDatensatz** -Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **NachschlagenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _In_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Datensatz für den Betrieb identifiziert. Das *im* Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.  <br/> |
| _Where Condition_ <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des **NachschlagenDatensatz** -Datenblocks wird ausgeführt. Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem. Kriterien nicht angegeben, wirkt sich auf die gesamte Domäne angegeben, die durch das Argument *In* das **NachschlagenDatensatz** -Datenblock. Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in *In* sein.  <br/> |
| _Alias_ <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument *im* angegebenen Datensatz enthält. Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen. Wenn *Alias* nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt. 
  
Wenn kein Datensatz erfüllt die *Bedingung* oder *In* keine Datensätze enthält, erstellt **NachschlagenDatensatz** einen leeren Datensatz in dem alle Felder einen **Null** -Wert enthalten. 
  


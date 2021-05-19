---
title: LookupRecord Data Block (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Mit einem NachschlagenDatensatz -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434361"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>LookupRecord Data Block (benutzerdefinierte Access-Web-App)

Mit einem **NachschlagenDatensatz** -Datenblock wird eine Reihe von Aktionen für einen bestimmten Datensatz ausgeführt. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **NachschlagenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Die **NachschlagenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _In_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Datensatz bezeichnet, für den eine Aktion ausgeführt werden soll. Das *Argument In* kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL enthalten.  <br/> |
| _Bedingung_ <br/> |Nein  <br/> |Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der **Datenblock LookupRecord** ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der **Datenblock LookupRecord** für die gesamte Domäne ausgeführt, die durch das  *Argument In angegeben*  wird. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in *sein.*  <br/> |
| _Alias_ <br/> |Nein  <br/> |Eine Zeichenfolge, die einen alternativen Namen für den durch das Argument In angegebenen  *Datensatz*  enthält. Wird häufig als Abkürzung des Tabellennamens in späteren Verweisen verwendet, um mögliche Mehrdeutigkeiten zu vermeiden. Wenn  *Alias*  nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn von den im  *In*  -Argument und im  *Bedingung*  -Argument angegebenen Kriterien mehrere Datensätze angegeben werden, wird der **NachschlagenDatensatz** -Datenblock nur für den ersten Datensatz ausgeführt. 
  
Wenn kein Datensatz  *Where Condition*  erfüllt oder  *Wenn In*  keine Datensätze enthält, erstellt **LookupRecord** einen leeren Datensatz, in dem alle Felder einen **Null-Wert** enthalten. 
  


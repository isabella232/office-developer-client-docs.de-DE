---
title: Var-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Gibt die statistische Varianz für eine Populationsstichprobe zurück, die als Satz von Werten dargestellt wird, die in einem angegebenen Feld einer Abfrage enthalten sind.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437756"
---
# <a name="var-function-access-custom-web-app"></a>Var-Funktion (Access Custom Web App)

Gibt die statistische Varianz für eine Populationsstichprobe zurück, die als Satz von Werten dargestellt wird, die in einem angegebenen Feld einer Abfrage enthalten sind.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Var** (*Numerischer Ausdruck*) 
  
Die **var** -Funktion enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Numerischer Ausdruck*  <br/> |Ein Textausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die ausgewertet werden sollen, oder ein Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld ausführt. Operanden in *numericive* können den Namen eines Tabellenfelds, eine Konstante oder eine Funktion enthalten (Dies kann entweder systeminterne oder benutzerdefinierte, aber nicht eine der anderen SQL-Aggregatfunktionen sein).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **Var** kann nur mit numerischen Spalten verwendet werden. Nullwerte werden ignoriert. 
  


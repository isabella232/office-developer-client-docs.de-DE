---
title: Choose-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790197"
---
# <a name="choose-function-access-custom-web-app"></a>Choose-Funktion (Access benutzerdefinierte Web app)

Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Wählen Sie aus** (*Indexnummer kann ein*, *Wert*[*Value_n*]) 
  
Die **Choose** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Indexnummer kann ein*  <br/> |Ein Integer-Ausdruck, der ein 1-basierter Indexwert in der Liste der folgenden Elemente darstellt.  <br/> |
| *Wert*  <br/> |Liste der Werte von einem beliebigen Datentyp.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der angegebenen *Indexnummer kann ein* nicht um eine ganze Zahl ist, wird der Wert auf eine Ganzzahl implizit konvertiert. 
  
Wenn der Indexwert die Grenzen des Arrays von Werte überschreitet, gibt **Choose** NULL zurück. 
  


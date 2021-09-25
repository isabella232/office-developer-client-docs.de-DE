---
title: Var-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Gibt die statistische Varianz für eine Stichprobe der Grundfüllung zurück, die als wertesatz dargestellt wird, der in einem angegebenen Feld in einer Abfrage enthalten ist.
ms.openlocfilehash: a6ce06ea74c32a52685d1debee14345b193920e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588392"
---
# <a name="var-function-access-custom-web-app"></a>Var-Funktion (benutzerdefinierte Access-Web-App)

Gibt die statistische Varianz für eine Stichprobe der Grundfüllung zurück, die als wertesatz dargestellt wird, der in einem angegebenen Feld in einer Abfrage enthalten ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Var** (*NumericExpression*) 
  
Die **Var-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *NumericExpression*  <br/> |Ein Textausdruck, der das Feld identifiziert, das die auszuwertenden numerischen Daten enthält, oder einen Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld durchführt. Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Konstante oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte Funktionen sein kann, jedoch keine der anderen SQL Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **"Var"** kann nur mit numerischen Spalten verwendet werden. Nullwerte werden ignoriert. 
  


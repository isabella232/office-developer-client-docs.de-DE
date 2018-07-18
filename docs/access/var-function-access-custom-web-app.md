---
title: Var-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Gibt die statistische Varianz für eine Populationsstichprobe als Menge von Werten zurück, die in einem angegebenen Feld einer Abfrage enthalten sind.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790385"
---
# <a name="var-function-access-custom-web-app"></a>Var-Funktion (Access benutzerdefinierte Web app)

Gibt die statistische Varianz für eine Populationsstichprobe als Menge von Werten zurück, die in einem angegebenen Feld einer Abfrage enthalten sind.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Var** (*NumericExpression*) 
  
Die **Var** -Funktion enthält das folgende Argument. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Ein Ausdruck, identifiziert das Feld mit den numerischen Daten, die ausgewertet werden soll, oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird. Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Konstante oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **Var** kann nur bei numerischen Spalten verwendet werden. NULL-Werte werden ignoriert. 
  


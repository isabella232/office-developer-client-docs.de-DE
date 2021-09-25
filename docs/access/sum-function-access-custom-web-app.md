---
title: Sum-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Gibt die Summe aller Werte im Ausdruck zurück.
ms.openlocfilehash: 2e6b75d256776e9552939e124410d258be1c0d74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605701"
---
# <a name="sum-function-access-custom-web-app"></a>Sum-Funktion (benutzerdefinierte Access-Web-App)

Gibt die Summe aller Werte im Ausdruck zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Sum** (*NumericExpression*) 
  
Die **Sum-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *NumericExpression*  <br/> |Ein Ausdruck, der das Feld identifiziert, das die hinzuzufügenden numerischen Daten enthält, oder ein Ausdruck, der eine Berechnung mithilfe der Daten in diesem Feld durchführt. Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Konstante oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte Funktionen sein kann, jedoch keine der anderen SQL Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **Sum-Funktion** ignoriert Datensätze, die Nullwerte enthalten. 
  
Die **Sum-Funktion** kann nur mit numerischen Spalten verwendet werden. 
  


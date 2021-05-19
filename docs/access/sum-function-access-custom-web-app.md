---
title: Sum-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Gibt die Summe aller Werte im Ausdruck zurück.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427101"
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
| *NumericExpression*  <br/> |Ein Ausdruck, der das Feld identifiziert, das die numerischen Daten enthält, die Sie hinzufügen möchten, oder ein Ausdruck, der eine Berechnung mit den Daten in diesem Feld ausführt. Operanden in *NumericExpression* können den Namen eines Tabellenfelds, einer Konstanten oder einer Funktion enthalten (die entweder systeminterne oder benutzerdefinierte, aber keine der anderen Aggregatfunktionen SQL sein kann).  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Sum-Funktion** ignoriert Datensätze, die Null-Werte enthalten. 
  
Die **Sum-Funktion** kann nur mit numerischen Spalten verwendet werden. 
  


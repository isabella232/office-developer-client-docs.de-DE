---
title: Teilzeichenfolgefunktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Teil eines Ausdrucks Text zurückgegeben.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790375"
---
# <a name="substring-function-access-custom-web-app"></a>Teilzeichenfolgefunktion (Access benutzerdefinierte Web app)

Teil eines Ausdrucks Text zurückgegeben.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Teilzeichenfolge** (*TextExpression*, *Starten*, *Länge*) 
  
Die **Teilzeichenfolge** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck.  <br/> |
| *Start*  <br/> |Ein Integer-Ausdruck, der angibt, an dem die zurückgegebenen Zeichen beginnen. Wenn Start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten Zeichen, die im Ausdruck angegeben ist. In diesem Fall ist die Anzahl der Zeichen, die zurückgegeben werden, den größten Wert entweder die Summe der Start + Length-1 oder 0. Wenn Start größer als die Anzahl der Zeichen im Wertausdruck ist, wird ein leere Ausdruck zurückgegeben.  <br/> |
| *Length*  <br/> |Eine positive ganze Zahl-Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden. Wenn Length negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet. Ist die Summe der Start als auch Length größer als die Anzahl der Zeichen im Ausdruck ist, wird der gesamten Wert Ausdruck Anfang am Anfang zurückgegeben.  <br/> |
   


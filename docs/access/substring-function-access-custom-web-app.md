---
title: SubString-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Gibt einen Teil eines Textausdrucks zurück.
ms.openlocfilehash: 74bd29717caa32aa9a8de5376ce7fc06bef02462
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614668"
---
# <a name="substring-function-access-custom-web-app"></a>SubString-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen Teil eines Textausdrucks zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
Die **SubString-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck.  <br/> |
| *Start*  <br/> |Ein ganzzahliger Ausdruck, der angibt, wo die zurückgegebenen Zeichen beginnen. Wenn Start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten im Ausdruck angegebenen Zeichen. In diesem Fall ist die Anzahl der zurückgegebenen Zeichen der größte Wert der Summe von Start + Länge - 1 oder 0. Wenn Start größer als die Anzahl der Zeichen im Wertausdruck ist, wird ein Ausdruck der Länge Null zurückgegeben.  <br/> |
| *Length*  <br/> |Ein positiver ganzzahliger Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden. Wenn die Länge negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet. Wenn die Summe von Start und Länge größer als die Anzahl der Zeichen im Ausdruck ist, wird der gesamte Wertausdruck zurückgegeben, der zu Beginn beginnt.  <br/> |
   


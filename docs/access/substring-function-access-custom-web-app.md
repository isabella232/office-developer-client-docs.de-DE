---
title: SubString-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Gibt einen Teil eines Textausdrucks zurück.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433472"
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
| *Start*  <br/> |Ein ganzzahliger Ausdruck, der angibt, wo die zurückgegebenen Zeichen beginnen. Wenn start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten Zeichen, das im Ausdruck angegeben ist. In diesem Fall ist die Anzahl der zurückgegebenen Zeichen der größte Wert der Summe start + length- 1 oder 0. Wenn start größer als die Anzahl der Zeichen im Wertausdruck ist, wird ein Ausdruck mit null Länge zurückgegeben.  <br/> |
| *Length*  <br/> |Ein positiver ganzzahliger Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden. Wenn die Länge negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet. Wenn die Summe von Start und Länge größer als die Anzahl der Zeichen im Ausdruck ist, wird der gesamte Wertausdruck zurückgegeben, der zu Beginn beginnt.  <br/> |
   


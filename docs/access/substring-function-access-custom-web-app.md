---
title: SUBSTRING-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Gibt einen Teil eines Text Ausdrucks zurück.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301694"
---
# <a name="substring-function-access-custom-web-app"></a>SUBSTRING-Funktion (Access Custom Web App)

Gibt einen Teil eines Text Ausdrucks zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 Teil **Zeichenfolge** (*Text*-, *Start*-, *Länge*) 
  
Die **SUBSTRING** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Text*  <br/> |Ein Textausdruck.  <br/> |
| *Start*  <br/> |Ein ganzzahliger Ausdruck, der angibt, wo die zurückgegebenen Zeichen beginnen. Wenn Start kleiner als 1 ist, beginnt der zurückgegebene Ausdruck mit dem ersten Zeichen, das in Expression angegeben ist. In diesem Fall ist die Anzahl der zurückgegebenen Zeichen der größte Wert der Summe von Start + Länge-1 oder 0. Wenn Start größer ist als die Anzahl der Zeichen im Wertausdruck, wird ein Ausdruck mit der Länge Null zurückgegeben.  <br/> |
| *Length*  <br/> |Ein positiver ganzzahliger Ausdruck, der angibt, wie viele Zeichen des Ausdrucks zurückgegeben werden. Wenn length negativ ist, wird ein Fehler generiert, und die Anweisung wird beendet. Wenn die Summe von Start und length größer als die Anzahl der Zeichen in Expression ist, wird der gesamte Wertausdruck, der bei Start beginnt, zurückgegeben.  <br/> |
   


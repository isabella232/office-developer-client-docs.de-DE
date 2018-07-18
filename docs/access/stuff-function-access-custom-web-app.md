---
title: Dinge-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in einer anderen Zeichenfolge. Löscht eine angegebene Anzahl von Zeichen in der ersten Zeichenfolge an der Startposition und klicken Sie dann in der ersten Zeichenfolge an der Startposition die zweite Zeichenfolge eingefügt.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790363"
---
# <a name="stuff-function-access-custom-web-app"></a>Dinge-Funktion (Access benutzerdefinierte Web app)

Fügt eine Textzeichenfolge in einer anderen Zeichenfolge. Löscht eine angegebene Anzahl von Zeichen in der ersten Zeichenfolge an der Startposition und klicken Sie dann in der ersten Zeichenfolge an der Startposition die zweite Zeichenfolge eingefügt.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Sammlung (engl.)** (*IntoTextExpression*, *Starten*, *Länge*, *ThisTextExpression*) 
  
Die **Dinge** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Ein Ausdruck, der den Text angibt, in dem der durch die *ThisTextExpression* angegebene Text eingefügt werden.  <br/> |
| *Start*  <br/> |Ein Ganzzahlwert, der den Speicherort zum Löschen und Einfügen begonnen angibt. Wenn Start oder Length negativ ist, wird eine null-Zeichenfolge zurückgegeben. Wenn Start länger als die erste *IntoTextExpression* ist, wird eine null-Zeichenfolge zurückgegeben.  <br/> |
| *Length*  <br/> |Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt. Wenn Length länger als die erste *IntoTextExpression* ist, erfolgt die Löschung bis zum letzten Zeichen in der letzten *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Hat einen Text-Ausdruck gibt den Text in *IntoTextExpression* einfügen. Dieser Ausdruck ersetzt Length Zeichen des *IntoTextExpression* , beginnend am *Starten* .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Argumente *Start* oder *Length* negativ sind oder die Startposition größer als die Länge der ersten Zeichenfolge ist, wird eine leere Zeichenfolge zurückgegeben. Wenn die Startposition 0 ist, wird ein Nullwert zurückgegeben. Wenn die Länge zu löschenden länger als die erste Zeichenfolge ist, wird es auf das erste Zeichen in der ersten Zeichenfolge gelöscht. 
  


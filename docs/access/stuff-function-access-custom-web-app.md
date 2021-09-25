---
title: Stuff-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
ms.openlocfilehash: f062ae87982b0c3811891b1fa9df777123c7478d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593047"
---
# <a name="stuff-function-access-custom-web-app"></a>Stuff-Funktion (benutzerdefinierte Access-Web-App)

Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*) 
  
Die **Funktion Stuff** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Ein Textausdruck, der den Text angibt, in den der durch  *ThisTextExpression*  angegebene Text eingefügt wird.  <br/> |
| *Start*  <br/> |Ein ganzzahliger Wert, der die Position angibt, an der mit dem Löschen und Einfügen begonnen werden soll. Wenn der Start oder die Länge negativ ist, wird eine Nullzeichenfolge zurückgegeben. Wenn Start länger als der erste  *IntoTextExpression*  ist, wird eine NULL-Zeichenfolge zurückgegeben.  <br/> |
| *Length*  <br/> |Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt. Wenn die Länge länger als die erste  *IntoTextExpression*  ist, erfolgt der Löschvorgang bis zum letzten Zeichen im letzten  *IntoTextExpression*  -Objekt.  <br/> |
| *ThisTextExpression*  <br/> |Ein Textausdruck hat gibt den Text an, der in  *IntoTextExpression*  eingefügt werden soll. Dieser Ausdruck ersetzt längenzeichen von  *IntoTextExpression*  beginnend bei  *Start*  .  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Argumente *Start* oder Length negativ sind oder die Anfangsposition größer als die Länge der ersten Zeichenfolge ist, wird eine Nullzeichenfolge zurückgegeben.  Wenn die Startposition 0 ist, wird ein NULL-Wert zurückgegeben. Wenn die zu löschende Länge länger als die erste Zeichenfolge ist, wird sie mit dem ersten Zeichen in der ersten Zeichenfolge gelöscht. 
  


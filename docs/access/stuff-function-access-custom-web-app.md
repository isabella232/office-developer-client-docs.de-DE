---
title: Stuff-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Sie löscht eine angegebene Zeichen Länge in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311025"
---
# <a name="stuff-function-access-custom-web-app"></a>Stuff-Funktion (Access Custom Web App)

Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Sie löscht eine angegebene Zeichen Länge in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Stuff** (*IntoTextExpression*, *Start*, *length*, *ThisTextExpression*) 
  
Die **stuff** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Ein Textausdruck, der den Text angibt, in den der durch das *ThisTextExpression* angegebene Text eingefügt wird.  <br/> |
| *Start*  <br/> |Ein ganzzahliger Wert, der die Position angibt, zu der gelöscht und eingefügt werden soll. Wenn Start oder length negativ ist, wird eine NULL-Zeichenfolge zurückgegeben. Wenn Start länger als der erste *IntoTextExpression* ist, wird eine NULL-Zeichenfolge zurückgegeben.  <br/> |
| *Length*  <br/> |Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt. Wenn length länger als der erste *IntoTextExpression* ist, wird der Löschvorgang bis zum letzten Zeichen im letzten *IntoTextExpression* ausgeführt.  <br/> |
| *ThisTextExpression*  <br/> |Ein Text Ausdrucks-Hut gibt den Text an, der in *IntoTextExpression* eingefügt werden soll. Dieser Ausdruck ersetzt die Länge der Zeichen von *IntoTextExpression* , die am Anfang *beginnen* .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Argumente *Start* oder *length* negativ sind oder wenn die Anfangsposition größer als die Länge der ersten Zeichenfolge ist, wird eine NULL-Zeichenfolge zurückgegeben. Wenn die Startposition 0 ist, wird ein NULL-Wert zurückgegeben. Wenn die zu löschende Länge länger als die erste Zeichenfolge ist, wird Sie in das erste Zeichen in der ersten Zeichenfolge gelöscht. 
  


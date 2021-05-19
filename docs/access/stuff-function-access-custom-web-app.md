---
title: Stuff-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427675"
---
# <a name="stuff-function-access-custom-web-app"></a>Stuff-Funktion (benutzerdefinierte Access-Web-App)

Fügt eine Textzeichenfolge in eine andere Textzeichenfolge ein. Es löscht eine angegebene Länge von Zeichen in der ersten Zeichenfolge an der Startposition und fügt dann die zweite Zeichenfolge in die erste Zeichenfolge an der Startposition ein.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*) 
  
Die **Stuff-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Ein Textausdruck, der den Text angibt, in den der durch  *thisTextExpression*  angegebene Text eingefügt wird.  <br/> |
| *Start*  <br/> |Ein ganzzahliger Wert, der die Position angibt, an der das Löschen und Einfügen gestartet werden soll. Wenn Start oder Länge negativ ist, wird eine Nullzeichenfolge zurückgegeben. Wenn start länger als der erste  *IntoTextExpression*  ist, wird eine Nullzeichenfolge zurückgegeben.  <br/> |
| *Length*  <br/> |Eine ganze Zahl, die die Anzahl der zu löschenden Zeichen angibt. Wenn die Länge länger als das erste *IntoTextExpression-Objekt ist,* erfolgt das Löschen bis zum letzten Zeichen im letzten *IntoTextExpression -Objekt.*  <br/> |
| *ThisTextExpression*  <br/> |Ein Textausdruckshut gibt den Text an, der in *IntoTextExpression eingefügt werden soll.* Dieser Ausdruck ersetzt Längenzeichen von *IntoTextExpression, die* bei *Start beginnen.*  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die  *Argumente Start*  oder  *Length*  negativ sind oder die Anfangsposition größer als die Länge der ersten Zeichenfolge ist, wird eine Nullzeichenfolge zurückgegeben. Wenn die Startposition 0 ist, wird ein Nullwert zurückgegeben. Wenn die zu löschende Länge länger als die erste Zeichenfolge ist, wird sie in das erste Zeichen in der ersten Zeichenfolge gelöscht. 
  


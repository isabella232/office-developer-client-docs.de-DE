---
title: IIf-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und wenn true, wenn eine andere einen Wert zurück, auf If "FALSE".
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790179"
---
# <a name="iif-function-access-custom-web-app"></a>IIf-Funktion (Access benutzerdefinierte Web app)

Überprüft, ob eine Bedingung erfüllt ist, und wenn true, wenn eine andere einen Wert zurück, auf If "FALSE".
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**IIf** (*Bedingung*, *TrueValue*, *FalseValue*) 
  
Die **IIf** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Bedingung*  <br/> |Der Ausdruck, den ausgewertet werden soll.  <br/> |
| *TrueValue*  <br/> |Wert oder-Ausdruck zurückgegeben, wenn *Bedingung* True ist.  <br/> |
| *FalseValue*  <br/> |Wert oder-Ausdruck zurückgegeben, wenn *Bedingung* auf false festgelegt ist.  <br/> |
   
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen angezeigt.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`



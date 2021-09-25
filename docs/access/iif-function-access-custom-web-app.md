---
title: IIf-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen Werts bei FALSE ist.
ms.openlocfilehash: 688c17434d9fb8843740989226f82b8a49ee1358
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593124"
---
# <a name="iif-function-access-custom-web-app"></a>IIf-Funktion (benutzerdefinierte Access-Web-App)

Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen Werts bei FALSE ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**IIf** (*Bedingung*, *TrueValue*, *FalseValue*) 
  
Die **IIf-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Bedingung*  <br/> |Der Ausdruck, den Sie auswerten möchten.  <br/> |
| *Truevalue*  <br/> |Zurückgegebener Wert oder Ausdruck, wenn  *Condition*  auf True festgelegt  <br/> |
| *Falsevalue*  <br/> |Zurückgegebener Wert oder Ausdruck, wenn  *Bedingung*  auf False festgelegt  <br/> |
   
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das MiddleInitial-Feld leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzuzeigen.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`



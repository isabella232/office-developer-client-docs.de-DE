---
title: IIf-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn dieser auf TRUE festgelegt ist.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301862"
---
# <a name="iif-function-access-custom-web-app"></a>IIf-Funktion (Access Custom Web App)

Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn dieser auf TRUE festgelegt ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
Die **IIf** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Bedingung*  <br/> |Der Ausdruck, den Sie auswerten möchten.  <br/> |
| *TrueValue*  <br/> |Wert oder Ausdruck, der zurückgegeben wird, wenn die *Bedingung* true ist.  <br/> |
| *FalseValue*  <br/> |Zurückgegebener Wert oder Ausdruck, wenn *Condition* auf false festgelegt ist.  <br/> |
   
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzuzeigen.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`



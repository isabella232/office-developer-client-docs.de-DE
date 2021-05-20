---
title: IIf-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen auf ist, wenn sie FALSE ist.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439079"
---
# <a name="iif-function-access-custom-web-app"></a>IIf-Funktion (benutzerdefinierte Access-Web-App)

Überprüft, ob eine Bedingung erfüllt ist, und gibt einen Wert zurück, wenn TRUE eines anderen auf ist, wenn sie FALSE ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
Die **IIf-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Bedingung*  <br/> |Der Ausdruck, den Sie auswerten möchten.  <br/> |
| *TrueValue*  <br/> |Wert oder Ausdruck zurückgegeben, wenn  *Condition*  true ist.  <br/> |
| *FalseValue*  <br/> |Zurückgegebener Wert oder Ausdruck, wenn  *Condition auf*  False gesetzt ist.  <br/> |
   
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzeigen zu können.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`



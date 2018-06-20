---
title: Try_Convert-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Konvertiert einen Wert in einem angegebenen Datentyp, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790395"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Try_Convert-Funktion (Access benutzerdefinierte Web app)

Konvertiert einen Wert in einem angegebenen Datentyp, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Try_Convert** (*Datentyp*, *Ausdruck*) 
  
Die **Try_Convert** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *DataType*  <br/> |Geben Sie die Daten in den *Ausdruck* konvertiert.  <br/> |
| *Expression*  <br/> |Der Wert konvertiert werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Try_Convert** nimmt den Wert übergeben wurden und versucht, in den angegebenen *Datentyp* zu konvertieren. Wenn die Konvertierung erfolgreich ist, gibt **Try_Convert** den Wert als den angegebenen *Datentyp* zurück; Wenn ein Fehler auftritt, wird Null zurückgegeben. Jedoch wenn Sie eine Konvertierung, die nicht explizit zulässig ist anfordern, schlägt **Try_Convert** mit einem Fehler. 
  


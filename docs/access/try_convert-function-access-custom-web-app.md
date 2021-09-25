---
title: Try_Convert-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Konvertiert einen Wert in einen angegebenen Datentyp oder gibt Null zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: 0e2aa0d877090812494c2aa53a3325ad2217eaa5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564680"
---
# <a name="try_convert-function-access-custom-web-app"></a>Try_Convert-Funktion (benutzerdefinierte Access-Web-App)

Konvertiert einen Wert in einen angegebenen Datentyp oder gibt Null zurück, wenn die Konvertierung ungültig ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Try_Convert** (*DataType*, *Expression*) 
  
Die **Try_Convert-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *DataType*  <br/> |Der Datentyp, in den  *Ausdruck*  konvertiert werden soll.  <br/> |
| *Ausdruck*  <br/> |Der zu konvertierende Wert.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **Try_Convert** übernimmt den übergebenen Wert und versucht, ihn in den angegebenen  *DataType*  zu konvertieren. Wenn die Konvertierung erfolgreich ist, **gibt Try_Convert** den Wert als angegebenen  *DataType zurück;*  wenn ein Fehler auftritt, wird NULL zurückgegeben. Wenn Sie jedoch eine Konvertierung anfordern, die explizit nicht zulässig ist, schlägt **Try_Convert** mit einem Fehler fehl. 
  


---
title: Try_Convert-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Konvertiert einen Wert in einen angegebenen Datentyp oder gibt NULL zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410896"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Try_Convert-Funktion (Access Custom Web App)

Konvertiert einen Wert in einen angegebenen Datentyp oder gibt NULL zurück, wenn die Konvertierung ungültig ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Try_Convert** (*DataType*, *Ausdruck*) 
  
Die **Try_Convert** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *DataType*  <br/> |Der Datentyp, in den *Ausdruck* konvertiert werden soll.  <br/> |
| *Ausdruck*  <br/> |Der zu konvertierende Wert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **Try_Convert** übernimmt den an Sie übergebenen Wert und versucht, Sie in den angegebenen *Datentyp* umzuwandeln. Wenn die Konvertierung erfolgreich ist, gibt **Try_Convert** den Wert als angegebenen *Datentyp* zurück. Wenn ein Fehler auftritt, wird NULL zurückgegeben. Wenn Sie jedoch eine Konvertierung anfordern, die explizit nicht zulässig ist, schlägt **Try_Convert** mit einem Fehler fehl. 
  


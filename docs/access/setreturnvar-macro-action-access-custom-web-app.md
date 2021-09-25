---
title: SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Die SetReturnVar-Aktion erstellt eine Rückgabevariable und legt sie auf einen bestimmten Wert fest.
ms.openlocfilehash: 0560ec9b1d4adbe215e5c187bcc1135c605b3ee9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614745"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)

Die **SetReturnVar-Aktion** erstellt eine Rückgabevariable und legt sie auf einen bestimmten Wert fest. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Die **SetReturnVar-Aktion** ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **SetReturnVar-Aktion** hat die folgenden Argumente. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _Name_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Namen der Variablen angibt.  <br/> |
| _Ausdruck_ <br/> |Ja  <br/> |Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die Schaltfläche **Erstellen** klicken, um das Argument mithilfe des **Ausdrucks-Generators** festzulegen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **SetReturnVar-Aktion** wird verwendet, um eine **ReturnVar**-Variable zu erstellen, die von Makros verwendet werden kann, die ein Datenmakro mithilfe der **RunDataMacro-Aktion** aufrufen. 
  
Nachdem ein **ReturnVar** durch die **SetReturnVar-Aktion** erstellt wurde, kann es vom aufrufenden Makro in einem Ausdruck verwendet werden. Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess** erstellt haben, können Sie die Variable mit der folgenden Syntax verwenden:
  
`=[ReturnVars]![UpdateSuccess]`

Die **SetReturnVar-Aktion** kann nur in benannten Datenmakros verwendet werden. Sie ist in Datenmakros, die an ein Datenmakroereignis angefügt sind, nicht verfügbar. 
  


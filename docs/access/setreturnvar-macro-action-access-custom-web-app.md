---
title: SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Mit der SetReturnVar-Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409594"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar-Makroaktion (benutzerdefinierte Access-Web-App)

Mit der **SetReturnVar** -Aktion wird eine Rückgabevariable erstellt und auf einen bestimmten Wert festgelegt. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Die **SetReturnVar** -Aktion ist nur in datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Die **SetReturnVar** -Aktion hat die folgenden Argumente. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _Name_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Namen der Variablen angibt.  <br/> |
| _Ausdruck_ <br/> |Ja  <br/> |Ein Ausdruck, mit dem der Wert für diese temporäre Variable festgelegt wird. Stellen Sie dem Ausdruck kein Gleichheitszeichen (=) voran. Sie können auf die Schaltfläche **Erstellen** klicken, um das Argument mithilfe des **Ausdrucks-Generators** festzulegen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **SetReturnVar** -Aktion wird verwendet, um eine **ReturnVar**zu erstellen, die von Makros verwendet werden kann, die ein datenmakro mithilfe der **ausführendatenmakro** -Aktion aufrufen. 
  
Nachdem ein **ReturnVar** durch die **SetReturnVar** -Aktion erstellt wurde, kann es in einem Ausdruck vom aufrufenden Makro verwendet werden. Wenn Sie beispielsweise einen **ReturnVar** mit dem Namen **UpdateSuccess**erstellt haben, können Sie die Variable mithilfe der folgenden Syntax verwenden:
  
`=[ReturnVars]![UpdateSuccess]`

Die **SetReturnVar** -Aktion kann nur in benannten datenmakros verwendet werden. Sie ist in datenmakros, die an ein datenmakro Ereignis angefügt sind, nicht verfügbar. 
  


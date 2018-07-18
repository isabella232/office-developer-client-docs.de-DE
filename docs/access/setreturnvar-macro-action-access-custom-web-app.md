---
title: SetReturnVar-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Die SetReturnVar-Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790381"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar-Makroaktion (Access benutzerdefinierte Web app)

Die **SetReturnVar** -Aktion erstellt eine Variable zurückgegebene und platziert es in einem bestimmten Wert. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Die **SetReturnVar** -Aktion ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Die **SetReturnVar** -Aktion hat die folgenden Argumente. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
| _Name_ <br/> |Ja  <br/> |Eine Zeichenfolge, die den Namen der Variablen angibt.  <br/> |
| _Expression_ <br/> |Ja  <br/> |Ein Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen. Setzen Sie den Ausdruck mit dem Gleichheitszeichen (=). Sie können klicken Sie auf die Schaltfläche **Erstellen** , um den **Ausdrucks-Generator** verwenden, um dieses Argument festzulegen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Aktion **SetReturnVar** dient zum Erstellen einer **ReturnVar**die Variable, die von Makros kann, die ein Datenmakro Aufrufen verwendet werden, indem Sie mit der **AusführenDatenmakro** -Aktion ist. 
  
Nach dem Erstellen einer **ReturnVar** durch die **SetReturnVar** -Aktion können Sie von das aufrufende Makro in einem Ausdruck verwenden. Angenommen, wenn Sie eine **ReturnVar** mit dem Namen **UpdateSuccess**erstellt, können die Variable Sie mithilfe der folgenden Syntax:
  
`=[ReturnVars]![UpdateSuccess]`

Die **SetReturnVar** -Aktion kann nur in benannten Datenmakros verwendet werden. Es ist nicht verfügbar in Datenmakros, die ein Ereignis eines Makro zugeordnet sind. 
  


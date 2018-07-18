---
title: Datenmakro DatensatzLöschen-Aktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Mit der DatensatzLöschen -Aktion können Sie einen Datensatz löschen.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790158"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Datenmakro DatensatzLöschen-Aktion (Access benutzerdefinierte Web app)

Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="setting"></a>Einstellung

Die **DatensatzLöschen** -Aktion hat die folgenden Argumente. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Datensatzalias** <br/> |Eine Zeichenfolge, die den zu löschenden Datensatz identifiziert. Wenn das Argument *Alias* nicht angegeben ist, wird der aktuelle Datensatz gelöscht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Beispielsweise verwenden Sie die folgende Syntax, um auf die zuletzt erstellte Datensatz zu verweisen: 
  
`[LastCreateRecordIdentity]`



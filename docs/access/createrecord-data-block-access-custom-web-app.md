---
title: DatensatzErstellen-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Das DatensatzErstellen-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790233"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>DatensatzErstellen-Datenblock (Access benutzerdefinierte Web app)

Mit dem **DatensatzErstellen** -Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> [!HINWEIS] Der **DatensatzErstellen** -Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Erstellen Sie Datensatz In** <br/> |Ja  <br/> |Der Name der Tabelle, in der der neue Datensatz erstellt werden soll  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die den Datensatz identifiziert. Sie können den Alias des Datensatzes zur Kennzeichnung verwenden  <br/> |
   
## <a name="remarks"></a>Hinweise

Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt. 
  
Nach der **DatensatzErstellen** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor ein Commit für der neue Datensatz ausgeführt wird. In einem **DatensatzErstellen** -Datenblock sind die folgenden Aktionen verfügbar. 
  
||
|:-----|
|[Abbrechendatensatzänderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Im Anschluss: Else-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Wenn mit der **DatensatzErstellen** -Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld** -Aktion den Wert eines Felds im neuen Datensatz an. 
  
Sie können eine **verwenden, wenn... Im Anschluss: Else** Anweisung Vorgänge ausführen auf der Grundlage einer Bedingung. 
  
Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet. 
  
Nachdem der neue Datensatz ein Commit ausgeführt wird, können Sie die lokale Variable **LastCreateRecordIdentity** den Eintrag entwickelt verwenden. Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen. 
  
`[LastCreateRecordIdentity].[AssignedTo]`



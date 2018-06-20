---
title: BearbeitenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Das BearbeitenDatensatz-Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790188"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>BearbeitenDatensatz-Datenblock (Access benutzerdefinierte Web app)

Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern. 
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> [!HINWEIS] Der **BearbeitenDatensatz** -Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Der **BearbeitenDatensatz** -Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Alias** <br/> |Eine Zeichenfolge zur Identifizierung der Eintrag bearbeiten. Wenn das Argument *Alias* nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Nachdem die **BearbeitenDatensatz** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor die Änderungen an den Datensatz ein Commit ausgeführt werden. Die folgenden Aktionen sind in einer **BearbeitenDatensatz** -Datenblock verfügbar. 
  
||
|:-----|
|[Abbrechendatensatzänderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Im Anschluss: Else-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[SetField-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an. 
  
Sie können eine **verwenden, wenn... Im Anschluss: Else** Anweisung Vorgänge ausführen auf der Grundlage einer Bedingung. 
  
Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet. 
  
Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen: 
  
`[LastCreateRecordIdentity].[AssignedTo]`



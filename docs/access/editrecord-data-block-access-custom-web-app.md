---
title: BearbeitenDatensatz-Datenblock (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Mit dem BearbeitenDatensatz -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.
ms.openlocfilehash: 8e179eb08d5624adb58a72576ac816126e0a8edc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621493"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>BearbeitenDatensatz-Datenblock (benutzerdefinierte Access-Web-App)

Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **BearbeitenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Der **BearbeitenDatensatz**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Alias** <br/> |Eine Zeichenfolge, mit der der zu bearbeitende Datensatz gekennzeichnet wird. Wenn das  *Alias-Argument*  nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nach der **EditRecord-Anweisung** können Sie einen Block von Befehlen einfügen, die ausgeführt werden, bevor für die Änderungen am Datensatz ein Commit ausgeführt wird. Die folgenden Aktionen sind in einem **EditRecord-Datenblock** verfügbar. 
  
||
|:-----|
|[AbbrechenDatensatzÄnderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[Wenn...Dann...Sonst-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[FestlegenFeld-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an. 
  
Sie können ein **If... Dann... Else-Anweisung** zum Ausführen von Vorgängen basierend auf einer Bedingung. 
  
Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet. 
  
Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf das AssignedTo-Feld des zuletzt erstellten Datensatzes zu verweisen: 
  
`[LastCreateRecordIdentity].[AssignedTo]`



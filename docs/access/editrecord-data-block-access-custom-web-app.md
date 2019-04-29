---
title: Bearbeitendatensatz-Daten Block (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Mit dem BearbeitenDatensatz -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418344"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Bearbeitendatensatz-Daten Block (Access Custom Web App)

Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **BearbeitenDatensatz**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Der **BearbeitenDatensatz**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|**Alias** <br/> |Eine Zeichenfolge, mit der der zu bearbeitende Datensatz gekennzeichnet wird. Wenn das Argument *Alias* nicht angegeben wird, wird der aktuelle Datensatz bearbeitet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Nach der **bearbeitendatensatz** -Anweisung können Sie einen Block von Befehlen Einfügen, die ausgeführt werden, bevor die Änderungen am Datensatz übernommen werden. Die folgenden Aktionen sind in einem **bearbeitendatensatz** -Datenblock verfügbar. 
  
||
|:-----|
|[AbbrechenDatensatzÄnderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[Wenn...Dann...Sonst-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[FestlegenFeld-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an. 
  
Sie können eine if.. **. Dann... Else** -Anweisung zum Ausführen von Vorgängen basierend auf einer Bedingung. 
  
Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet. 
  
Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf das Feld ZugewiesenAn des zuletzt erstellten Datensatzes zu verweisen: 
  
`[LastCreateRecordIdentity].[AssignedTo]`



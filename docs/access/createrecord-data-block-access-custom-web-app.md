---
title: CreateRecord Data Block (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Mit dem DatensatzErstellen-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421375"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord Data Block (benutzerdefinierte Access-Web-App)

Mit dem **DatensatzErstellen**-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **DatensatzErstellen**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Setting

Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Datensatz erstellen in** <br/> |Ja  <br/> |Der Name der Tabelle, in der der neue Datensatz erstellt werden soll  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die den Datensatz identifiziert. Sie können den Alias des Datensatzes zur Kennzeichnung verwenden  <br/> |
   
## <a name="remarks"></a>Hinweise

Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt. 
  
Nach **der CreateRecord-Anweisung** können Sie einen Befehlsblock einfügen, der ausgeführt wird, bevor der neue Datensatz ausgeführt wird. In einem **DatensatzErstellen**-Datenblock sind die folgenden Aktionen verfügbar. 
  
||
|:-----|
|[AbbrechenDatensatzänderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[Wenn...Dann...Sonst-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[FestlegenFeld-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Wenn mit der **DatensatzErstellen**-Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld**-Aktion den Wert eines Felds im neuen Datensatz an. 
  
Sie können eine **If... Dann... Else-Anweisung** zum Ausführen von Vorgängen basierend auf einer Bedingung. 
  
Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet. 
  
Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. Verwenden Sie beispielsweise die folgende Syntax, um auf das AssignedTo-Feld des zuletzt erstellten Datensatzes zu verweisen. 
  
`[LastCreateRecordIdentity].[AssignedTo]`



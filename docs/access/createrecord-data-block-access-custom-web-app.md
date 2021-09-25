---
title: CreateRecord Data Block (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Mit dem DatensatzErstellen-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.
ms.openlocfilehash: 7d604d80f1ba71c975151a9a46f38b3995c64bae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573362"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord Data Block (Benutzerdefinierte Access-Web-App)

Mit dem **DatensatzErstellen**-Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen. 
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
> [!NOTE]
> Der **DatensatzErstellen**-Datenblock ist nur in Datenmakros verfügbar. 
  
## <a name="setting"></a>Einstellung

Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden. 
  
|**Argumentname**|**Erforderlich**|**Beschreibung**|
|:-----|:-----|:-----|
|**Datensatz erstellen in** <br/> |Ja  <br/> |Der Name der Tabelle, in der der neue Datensatz erstellt werden soll  <br/> |
|**Alias** <br/> |Nein  <br/> |Eine Zeichenfolge, die den Datensatz identifiziert. Sie können den Alias des Datensatzes zur Kennzeichnung verwenden  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt. 
  
Nach **der CreateRecord-Anweisung** können Sie einen Befehlsblock einfügen, der ausgeführt wird, bevor für den neuen Datensatz ein Commit ausgeführt wird. In einem **DatensatzErstellen**-Datenblock sind die folgenden Aktionen verfügbar. 
  
||
|:-----|
|[AbbrechenDatensatzänderung-Makroaktion](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Kommentar-Makroanweisung](comment-macro-block-access-custom-web-app.md) <br/> |
|[Gruppieren-Makroanweisung](group-macro-block-access-custom-web-app.md) <br/> |
|[Wenn...Dann...Sonst-Makroanweisung](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[FestlegenFeld-Makroaktion](setfield-macro-action-access-custom-web-app.md) <br/> |
|[FestlegenLokaleVar-Makroaktion](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Wenn mit der **DatensatzErstellen**-Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld**-Aktion den Wert eines Felds im neuen Datensatz an. 
  
Sie können ein **If... Dann... Else-Anweisung** zum Ausführen von Vorgängen basierend auf einer Bedingung. 
  
Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet. 
  
Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record. Verwenden Sie beispielsweise die folgende Syntax, um auf das Feld AssignedTo des zuletzt erstellten Datensatzes zu verweisen. 
  
`[LastCreateRecordIdentity].[AssignedTo]`



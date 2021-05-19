---
title: EditRecord Data Block (benutzerdefinierte Access-Web-App)
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
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="8872b-103">EditRecord Data Block (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="8872b-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="8872b-104">Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.</span><span class="sxs-lookup"><span data-stu-id="8872b-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8872b-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="8872b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8872b-107">Der **BearbeitenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8872b-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8872b-108">Setting</span><span class="sxs-lookup"><span data-stu-id="8872b-108">Setting</span></span>

<span data-ttu-id="8872b-109">Der **BearbeitenDatensatz**-Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8872b-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="8872b-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="8872b-110">**Argument**</span></span>|<span data-ttu-id="8872b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8872b-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8872b-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="8872b-112">**Alias**</span></span> <br/> |<span data-ttu-id="8872b-113">Eine Zeichenfolge, mit der der zu bearbeitende Datensatz gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8872b-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="8872b-114">Wenn das  *Argument Alias*  nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="8872b-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8872b-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8872b-115">Remarks</span></span>

<span data-ttu-id="8872b-116">Nach der **EditRecord -Anweisung** können Sie einen Befehlsblock einfügen, der ausgeführt wird, bevor die Änderungen am Datensatz ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8872b-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="8872b-117">Die folgenden Aktionen sind in einem **EditRecord-Datenblock** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8872b-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="8872b-118">AbbrechenDatensatzÄnderung-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8872b-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="8872b-119">Kommentar-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="8872b-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="8872b-120">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="8872b-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="8872b-121">Wenn...Dann...Sonst-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="8872b-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="8872b-122">FestlegenFeld-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8872b-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="8872b-123">FestlegenLokaleVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8872b-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="8872b-124">Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="8872b-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="8872b-125">Sie können eine **If... Dann... Else-Anweisung** zum Ausführen von Vorgängen basierend auf einer Bedingung.</span><span class="sxs-lookup"><span data-stu-id="8872b-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="8872b-p104">Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet.</span><span class="sxs-lookup"><span data-stu-id="8872b-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="8872b-128">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8872b-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="8872b-129">Verwenden Sie beispielsweise die folgende Syntax, um auf das AssignedTo-Feld des zuletzt erstellten Datensatzes zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="8872b-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`



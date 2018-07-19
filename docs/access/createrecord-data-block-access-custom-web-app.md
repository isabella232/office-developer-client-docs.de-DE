---
title: DatensatzErstellen-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Mit dem DatensatzErstellen -Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790233"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="bb0e8-103">DatensatzErstellen-Datenblock (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="bb0e8-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="bb0e8-104">Mit dem **DatensatzErstellen** -Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bb0e8-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bb0e8-107"> Der **DatensatzErstellen** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="bb0e8-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="bb0e8-108">Setting</span></span>

<span data-ttu-id="bb0e8-109">Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="bb0e8-110">Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="bb0e8-111">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-111">**Argument name**</span></span>|<span data-ttu-id="bb0e8-112">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-112">**Required**</span></span>|<span data-ttu-id="bb0e8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb0e8-114">**Datensatz erstellen in**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="bb0e8-115">Ja</span><span class="sxs-lookup"><span data-stu-id="bb0e8-115">Yes</span></span>  <br/> |<span data-ttu-id="bb0e8-116">Der Name der Tabelle, in der der neue Datensatz erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="bb0e8-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="bb0e8-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="bb0e8-117">**Alias**</span></span> <br/> |<span data-ttu-id="bb0e8-118">Nein</span><span class="sxs-lookup"><span data-stu-id="bb0e8-118">No</span></span>  <br/> |<span data-ttu-id="bb0e8-119">Eine Zeichenfolge, die den Datensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-119">A string that identifies the record.</span></span> <span data-ttu-id="bb0e8-120">Sie können den Alias des Datensatzes zur Kennzeichnung verwenden</span><span class="sxs-lookup"><span data-stu-id="bb0e8-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb0e8-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bb0e8-121">Remarks</span></span>

<span data-ttu-id="bb0e8-122">Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="bb0e8-123">Nach der **DatensatzErstellen** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor ein Commit für der neue Datensatz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="bb0e8-124">In einem **DatensatzErstellen** -Datenblock sind die folgenden Aktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="bb0e8-125">AbbrechenDatensatzänderung-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="bb0e8-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bb0e8-126">Kommentar-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="bb0e8-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bb0e8-127">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="bb0e8-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bb0e8-128">If... Im Anschluss: Else-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="bb0e8-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bb0e8-129">FestlegenFeld-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="bb0e8-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="bb0e8-130">FestlegenLokaleVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="bb0e8-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="bb0e8-131">Wenn mit der **DatensatzErstellen** -Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld** -Aktion den Wert eines Felds im neuen Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="bb0e8-132">Sie können eine **verwenden, wenn... Im Anschluss: Else** Anweisung Vorgänge ausführen auf der Grundlage einer Bedingung.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="bb0e8-p104">Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-p104">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="bb0e8-135">Nachdem der neue Datensatz ein Commit ausgeführt wird, können Sie die lokale Variable **LastCreateRecordIdentity** den Eintrag entwickelt verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="bb0e8-136">Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="bb0e8-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`



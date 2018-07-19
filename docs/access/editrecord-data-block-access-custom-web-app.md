---
title: BearbeitenDatensatz-Datenblock (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Mit dem BearbeitenDatensatz -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790188"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="931db-103">BearbeitenDatensatz-Datenblock (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="931db-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="931db-104">Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.</span><span class="sxs-lookup"><span data-stu-id="931db-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="931db-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="931db-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="931db-107"> Der **BearbeitenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="931db-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="931db-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="931db-108">Setting</span></span>

<span data-ttu-id="931db-109">Der **BearbeitenDatensatz** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="931db-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="931db-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="931db-110">**Argument**</span></span>|<span data-ttu-id="931db-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="931db-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="931db-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="931db-112">**Alias**</span></span> <br/> |<span data-ttu-id="931db-113">Eine Zeichenfolge zur Identifizierung der Eintrag bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="931db-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="931db-114">Wenn das Argument *Alias* nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="931db-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="931db-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="931db-115">Remarks</span></span>

<span data-ttu-id="931db-116">Nachdem die **BearbeitenDatensatz** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor die Änderungen an den Datensatz ein Commit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="931db-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="931db-117">Die folgenden Aktionen sind in einer **BearbeitenDatensatz** -Datenblock verfügbar.</span><span class="sxs-lookup"><span data-stu-id="931db-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="931db-118">AbbrechenDatensatzänderung-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="931db-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="931db-119">Kommentar-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="931db-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="931db-120">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="931db-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="931db-121">If... Im Anschluss: Else-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="931db-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="931db-122">FestlegenFeld-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="931db-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="931db-123">FestlegenLokaleVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="931db-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="931db-124">Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="931db-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="931db-125">Sie können eine **verwenden, wenn... Im Anschluss: Else** Anweisung Vorgänge ausführen auf der Grundlage einer Bedingung.</span><span class="sxs-lookup"><span data-stu-id="931db-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="931db-p104">Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet.</span><span class="sxs-lookup"><span data-stu-id="931db-p104">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="931db-128">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="931db-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="931db-129">Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="931db-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`



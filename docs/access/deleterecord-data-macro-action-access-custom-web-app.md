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
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="1607b-103">Datenmakro DatensatzLöschen-Aktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="1607b-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="1607b-104">Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen.</span><span class="sxs-lookup"><span data-stu-id="1607b-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1607b-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="1607b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1607b-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1607b-107">Setting</span></span>

<span data-ttu-id="1607b-108">Die **DatensatzLöschen** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="1607b-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1607b-109">**Argument**</span><span class="sxs-lookup"><span data-stu-id="1607b-109">**Argument**</span></span>|<span data-ttu-id="1607b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1607b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1607b-111">**Datensatzalias**</span><span class="sxs-lookup"><span data-stu-id="1607b-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="1607b-112">Eine Zeichenfolge, die den zu löschenden Datensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1607b-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="1607b-113">Wenn das Argument *Alias* nicht angegeben ist, wird der aktuelle Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1607b-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1607b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1607b-114">Remarks</span></span>

<span data-ttu-id="1607b-115">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1607b-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="1607b-116">Beispielsweise verwenden Sie die folgende Syntax, um auf die zuletzt erstellte Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="1607b-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`



---
title: DeleteRecord Data Macro-Aktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Mit der DatensatzLöschen -Aktion können Sie einen Datensatz löschen.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423153"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="1fefb-103">DeleteRecord Data Macro-Aktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="1fefb-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="1fefb-104">Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen.</span><span class="sxs-lookup"><span data-stu-id="1fefb-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1fefb-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="1fefb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1fefb-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1fefb-107">Setting</span></span>

<span data-ttu-id="1fefb-108">Die **DeleteRecord-Aktion** hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="1fefb-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="1fefb-109">**Argument**</span><span class="sxs-lookup"><span data-stu-id="1fefb-109">**Argument**</span></span>|<span data-ttu-id="1fefb-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fefb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fefb-111">**Datensatzalias**</span><span class="sxs-lookup"><span data-stu-id="1fefb-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="1fefb-112">Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1fefb-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="1fefb-113">Wenn das  *Alias-Argument*  nicht angegeben ist, wird der aktuelle Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1fefb-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fefb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fefb-114">Remarks</span></span>

<span data-ttu-id="1fefb-115">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1fefb-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="1fefb-116">Verwenden Sie beispielsweise die folgende Syntax, um auf den zuletzt erstellten Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="1fefb-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`



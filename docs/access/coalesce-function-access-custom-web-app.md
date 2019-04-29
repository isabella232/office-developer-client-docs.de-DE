---
title: ZusammenFügungsfunktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Gibt den ersten Ausdruck, der nicht NULL ist, aus einer Liste von Argumenten zurück.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411393"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="ba7fe-103">ZusammenFügungsfunktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="ba7fe-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="ba7fe-104">Gibt den ersten Ausdruck, der nicht NULL ist, aus einer Liste von Argumenten zurück.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ba7fe-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ba7fe-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ba7fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7fe-107">Syntax</span></span>

<span data-ttu-id="ba7fe-108">**Verschmelzen** (*Wert*, [*Wert*],..., [*Wert*])</span><span class="sxs-lookup"><span data-stu-id="ba7fe-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="ba7fe-109">Die **verschmelzen** -Funktion enthält die folgenden Argumente</span><span class="sxs-lookup"><span data-stu-id="ba7fe-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="ba7fe-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="ba7fe-110">**Argument name**</span></span>|<span data-ttu-id="ba7fe-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba7fe-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ba7fe-112">*Wert*</span><span class="sxs-lookup"><span data-stu-id="ba7fe-112">*Value*</span></span>  <br/> |<span data-ttu-id="ba7fe-113">Ein Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba7fe-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba7fe-114">Remarks</span></span>

<span data-ttu-id="ba7fe-115">Wenn alle Argumente NULL sind, \*\*\*\* gibt verschmelzen NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ba7fe-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ba7fe-116">Example</span></span>

<span data-ttu-id="ba7fe-117">Der folgende Ausdruck wird als Gültigkeitsprüfungsregel für eine Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="ba7fe-118">Der Ausdruck stellt sicher, dass die Einträge in den Feldern vorName, Nachname, E-Mail, Mobiltelefon, Telefon, privat Telefon und Unternehmen vorgenommen werden, bevor ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="ba7fe-119">Wenn eines der aufgelisteten Felder leer bleibt, gibt \*\*\*\* die Zusammenführungsfunktion NULL zurück, die gegen die Validierungsregel verstößt.</span><span class="sxs-lookup"><span data-stu-id="ba7fe-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



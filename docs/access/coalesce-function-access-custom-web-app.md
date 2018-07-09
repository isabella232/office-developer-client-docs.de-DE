---
title: COALESCE-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Gibt den ersten Ausdruck, der nicht aus einer Liste der Argumente NULL ist.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790201"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="bdf00-103">COALESCE-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="bdf00-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="bdf00-104">Gibt den ersten Ausdruck, der nicht aus einer Liste der Argumente NULL ist.</span><span class="sxs-lookup"><span data-stu-id="bdf00-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bdf00-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="bdf00-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bdf00-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdf00-107">Syntax</span></span>

<span data-ttu-id="bdf00-108">**Koaleszieren (COALESCE)** (*Wert*[*Wert*],..., [*Wert*])</span><span class="sxs-lookup"><span data-stu-id="bdf00-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="bdf00-109">**Coalesce** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="bdf00-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="bdf00-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="bdf00-110">**Argument name**</span></span>|<span data-ttu-id="bdf00-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdf00-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bdf00-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="bdf00-112">*Value*</span></span>  <br/> |<span data-ttu-id="bdf00-113">Ein Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="bdf00-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdf00-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdf00-114">Remarks</span></span>

<span data-ttu-id="bdf00-115">Wenn alle Argumente NULL sind, gibt **Coalesce** NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="bdf00-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bdf00-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bdf00-116">Example</span></span>

<span data-ttu-id="bdf00-117">Der folgende Ausdruck ist als der Überprüfungsregel für eine Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdf00-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="bdf00-118">Der Ausdruck wird sichergestellt, dass Einträge in den Feldern Vorname, letzte Name, E-Mail, Mobiltelefon, Arbeit, Home Phone, und Telefongesellschaft vorgenommen werden, bevor ein Datensatz ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf00-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="bdf00-119">Wenn eines der aufgelisteten Felder leer sind, gibt die **Coalesce** -Funktion Null, der die Gültigkeitsregel verletzen.</span><span class="sxs-lookup"><span data-stu-id="bdf00-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



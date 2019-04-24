---
title: Append-Methode (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297046"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="edeee-102">Append-Methode (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="edeee-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="edeee-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="edeee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edeee-104">Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="edeee-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="edeee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edeee-105">Syntax</span></span>

<span data-ttu-id="edeee-106">*Ansichten*. Append*Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="edeee-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="edeee-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="edeee-107">Parameters</span></span>

|<span data-ttu-id="edeee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="edeee-108">Parameter</span></span>|<span data-ttu-id="edeee-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edeee-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="edeee-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="edeee-110">*Name*</span></span> |<span data-ttu-id="edeee-111">Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.</span><span class="sxs-lookup"><span data-stu-id="edeee-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="edeee-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="edeee-112">*Command*</span></span> |<span data-ttu-id="edeee-113">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="edeee-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="edeee-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="edeee-114">Remarks</span></span>

<span data-ttu-id="edeee-115">Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command**-Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="edeee-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="edeee-p101">Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="edeee-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="edeee-p102">Beim Verwenden des OLE DB-Anbieters für Microsoft Jet und der **Append**-Methode der **Views**-Auflistung können Sie im *Command*-Parameter ein **Procedure**-Objekt statt eines **View**-Objekts angeben. Das **Procedure**-Objekt wird der Datenquelle und der **Views**-Auflistung hinzugefügt. Wenn die **Procedures**- und die **Views**-Auflistung nach Ausführung von **Append** aktualisiert wurden, wird das **Procedure**-Objekt nicht mehr in der **Views**-Auflistung, sondern in der **Procedures**-Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edeee-p102">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter. The **Procedure** will be added to the data source and will be added to the **Views** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>



---
title: Append-Methode (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474383"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="e3d98-102">Append-Methode (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="e3d98-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="e3d98-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3d98-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e3d98-104">Erstellt ein neues [View](view-object-adox.md)-Objekt und fügt es an die [Views](views-collection-adox.md)-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="e3d98-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d98-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3d98-105">Syntax</span></span>

<span data-ttu-id="e3d98-106">*Ansichten*. Fügen Sie*Namen*, *Befehl*</span><span class="sxs-lookup"><span data-stu-id="e3d98-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="e3d98-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d98-107">Parameters</span></span>

  - <span data-ttu-id="e3d98-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="e3d98-108">*Name*</span></span>

  - <span data-ttu-id="e3d98-109">Ein **String** -Wert, der den Namen der zu erstellenden Sicht angibt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="e3d98-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="e3d98-110">*Command*</span></span>

  - <span data-ttu-id="e3d98-111">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d98-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3d98-112">Remarks</span></span>

<span data-ttu-id="e3d98-113">Erstellt eine neue Sicht in der Datenquelle mit dem Namen und Attributen, die im **Command** -Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e3d98-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="e3d98-p101">Wenn der vom Benutzer angegebene Befehlstext keine Sicht, sondern eine Prozedur darstellt, ist das Verhalten vom Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e3d98-116">Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die <STRONG>Append</STRONG> -Methode der <STRONG>Views</STRONG> -Auflistung angeben einer <STRONG>Ansicht</STRONG> , sondern eine <STRONG>Prozedur</STRONG> in <EM>der Befehlsparameter</EM> ansetzt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="e3d98-117">Das <STRONG>Procedure</STRONG> -Objekt wird der Datenquelle und der <STRONG>Views</STRONG> -Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="e3d98-118">Wenn die <STRONG>Procedures</STRONG> - und die <STRONG>Views</STRONG> -Auflistung nach Ausführung von <STRONG>Append</STRONG> aktualisiert wurden, wird das <STRONG>Procedure</STRONG> -Objekt nicht mehr in der <STRONG>Views</STRONG> -Auflistung, sondern in der <STRONG>Procedures</STRONG> -Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3d98-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>



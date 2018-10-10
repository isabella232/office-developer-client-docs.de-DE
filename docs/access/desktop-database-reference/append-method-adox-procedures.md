---
title: Append-Methode (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473002"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="0b8f5-102">Append-Methode (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="0b8f5-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="0b8f5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b8f5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="0b8f5-104">Fügt der [Procedures](procedure-object-adox.md)-Auflistung ein neues [Procedure](procedures-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b8f5-105">Syntax</span></span>

<span data-ttu-id="0b8f5-106">*Verfahren*. Fügen Sie*Namen*, *Befehl*</span><span class="sxs-lookup"><span data-stu-id="0b8f5-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="0b8f5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b8f5-107">Parameters</span></span>

  - <span data-ttu-id="0b8f5-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="0b8f5-108">*Name*</span></span>

  - <span data-ttu-id="0b8f5-109">Ein **String** -Wert, der den Namen der zu erstellenden und anzufügenden Prozedur angibt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="0b8f5-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="0b8f5-110">*Command*</span></span>

  - <span data-ttu-id="0b8f5-111">Ein ADO-[Command](command-object-ado.md)-Objekt, das die zu erstellende und anzufügende Prozedur darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8f5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b8f5-112">Remarks</span></span>

<span data-ttu-id="0b8f5-113">Erstellt eine neue Prozedur in der Datenquelle mit dem Namen und den Attributen, die im **Command** -Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="0b8f5-p101">Wenn der vom Benutzer angegebene Befehlstext eine Sicht statt einer Prozedur darstellt, ist das Verhalten vom jeweils verwendeten Anbieter abhängig. Bei der Ausführung von **Append** tritt ein Fehler auf, wenn der Anbieter keine persistenten Befehle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b8f5-116">Wenn Sie den OLE DB-Anbieter für Microsoft Jet verwenden, kann die <STRONG>Append</STRONG> -Methode der <STRONG>Procedures</STRONG> -Auflistung angeben einer <STRONG>Ansicht</STRONG> , sondern eine <STRONG>Prozedur</STRONG> in <EM>der Befehlsparameter</EM> ansetzt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="0b8f5-117">Das <STRONG>View</STRONG> -Objekt wird der Datenquelle und der <STRONG>Procedures</STRONG> -Auflistung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="0b8f5-118">Wenn die <STRONG>Procedures</STRONG> - und die <STRONG>Views</STRONG> -Auflistung nach Ausführung von <STRONG>Append</STRONG> aktualisiert wurden, wird das <STRONG>View</STRONG> -Objekt nicht mehr in der <STRONG>Procedures</STRONG> -Auflistung, sondern in der <STRONG>Views</STRONG> -Auflistung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b8f5-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>



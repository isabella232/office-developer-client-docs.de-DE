---
title: ParentURL-Eigenschaft (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707815"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="cbccf-102">ParentURL-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="cbccf-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="cbccf-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbccf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbccf-104">Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete [Record](record-object-ado.md)-Objekt des aktuellen **Record** -Objekts verweist.</span><span class="sxs-lookup"><span data-stu-id="cbccf-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbccf-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbccf-105">Return value</span></span>

<span data-ttu-id="cbccf-106">Gibt einen **String** -Wert zurück, der die URL des übergeordneten **Record** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbccf-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbccf-107">Remarks</span></span>

<span data-ttu-id="cbccf-p101">Die **ParentURL** -Eigenschaft hängt von der Quelle ab, die zum Öffnen des **Record** -Objekts verwendet wird. Das **Record** -Objekt kann beispielsweise mit einer Quelle geöffnet werden, die einen relativen Pfadnamen eines Verzeichnisses enthält, auf das von der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cbccf-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="cbccf-p102">Angenommen, "second" ist ein Ordner, der unter "first" enthalten ist. Öffnen Sie das **Record** -Objekt folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="cbccf-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="cbccf-112">Nun, der Wert der **ParentURL** -Eigenschaft ist **ParentURL** -Eigenschaft ist "https://first", genau wie **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="cbccf-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="cbccf-113">Die Quelle kann auch eine absolute URL sein, wie z. B. "https://first/second".</span><span class="sxs-lookup"><span data-stu-id="cbccf-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="cbccf-114">**ParentURL** -Eigenschaft ist "https://first", die Ebene über.</span><span class="sxs-lookup"><span data-stu-id="cbccf-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="cbccf-115">**ParentURL** -Eigenschaft ist "https://first", die Ebene über "Sekunde".</span><span class="sxs-lookup"><span data-stu-id="cbccf-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="cbccf-116">Diese Eigenschaft kann in den folgenden Fällen ein Nullwert sein:</span><span class="sxs-lookup"><span data-stu-id="cbccf-116">This property may be a null value if:</span></span>

- <span data-ttu-id="cbccf-117">Für das aktuelle Objekt gibt es kein übergeordnetes Objekt. Beispiel: Wenn das **Record** -Objekt den Stamm eines Verzeichnisses darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="cbccf-118">Das **Record** -Objekt stellt eine Entität dar, die mit einer URL nicht angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbccf-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="cbccf-119">Die Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cbccf-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="cbccf-p104">[!HINWEIS] Diese Eigenschaft wird nur von Dokumentquellenanbietern wie z. B. [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) unterstützt. Weitere Informationen finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="cbccf-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="cbccf-122">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der Microsoft OLE DB Provider für Internet Publishing automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cbccf-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="cbccf-123">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="cbccf-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="cbccf-124">[!HINWEIS] Enthält der aktuelle Datensatz einen Datensatz aus einem ADO- **Recordset** -Objekt, verursacht der Zugriff auf die **ParentURL** -Eigenschaft einen Laufzeitfehler, der angibt, dass keine URL möglich ist.</span><span class="sxs-lookup"><span data-stu-id="cbccf-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>



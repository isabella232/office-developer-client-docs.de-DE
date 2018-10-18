---
<span data-ttu-id="22422-101"><<<<<<< HEAD-Titel: ParentURL-Eigenschaft (ADO) TOCTitle: ParentURL-Eigenschaft (ADO) === Titel: ParentURL-Eigenschaft (ADO) TOCTitle: ParentURL-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22422-101"><<<<<<< HEAD title: ParentURL Property (ADO) TOCTitle: ParentURL Property (ADO) ======= title: ParentURL property (ADO) TOCTitle: ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="22422-102">Master Ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) Ms:contentKeyID: 48548517 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="22422-102">master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="22422-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="22422-103"><<<<<<< HEAD</span></span>
# <a name="parenturl-property-ado"></a><span data-ttu-id="22422-104">ParentURL-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22422-104">ParentURL Property (ADO)</span></span>
=======
# <a name="parenturl-property-ado"></a><span data-ttu-id="22422-105">ParentURL-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="22422-105">ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="22422-106">master</span><span class="sxs-lookup"><span data-stu-id="22422-106">master</span></span>

<span data-ttu-id="22422-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22422-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22422-108">Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete [Record](record-object-ado.md)-Objekt des aktuellen **Record** -Objekts verweist.</span><span class="sxs-lookup"><span data-stu-id="22422-108">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

<span data-ttu-id="22422-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="22422-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="22422-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22422-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="22422-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22422-111">Return value</span></span>
>>>>>>> <span data-ttu-id="22422-112">master</span><span class="sxs-lookup"><span data-stu-id="22422-112">master</span></span>

<span data-ttu-id="22422-113">Gibt einen **String** -Wert zurück, der die URL des übergeordneten **Record** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="22422-113">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="22422-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22422-114">Remarks</span></span>

<span data-ttu-id="22422-p101">Die **ParentURL** -Eigenschaft hängt von der Quelle ab, die zum Öffnen des **Record** -Objekts verwendet wird. Das **Record** -Objekt kann beispielsweise mit einer Quelle geöffnet werden, die einen relativen Pfadnamen eines Verzeichnisses enthält, auf das von der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="22422-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="22422-p102">Angenommen, "second" ist ein Ordner, der unter "first" enthalten ist. Öffnen Sie das **Record** -Objekt folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="22422-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="22422-119">Nun, der Wert der **ParentURL** -Eigenschaft ist **ParentURL** -Eigenschaft ist "https://first", genau wie **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="22422-119">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="22422-120">Die Quelle kann auch eine absolute URL sein, wie z. B. "https://first/second".</span><span class="sxs-lookup"><span data-stu-id="22422-120">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="22422-121">**ParentURL** -Eigenschaft ist "https://first", die Ebene über.</span><span class="sxs-lookup"><span data-stu-id="22422-121">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="22422-122">**ParentURL** -Eigenschaft ist "https://first", die Ebene über "Sekunde".</span><span class="sxs-lookup"><span data-stu-id="22422-122">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="22422-123">Diese Eigenschaft kann in den folgenden Fällen ein Nullwert sein:</span><span class="sxs-lookup"><span data-stu-id="22422-123">This property may be a null value if:</span></span>

- <span data-ttu-id="22422-124">Für das aktuelle Objekt gibt es kein übergeordnetes Objekt. Beispiel: Wenn das **Record** -Objekt den Stamm eines Verzeichnisses darstellt.</span><span class="sxs-lookup"><span data-stu-id="22422-124">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="22422-125">Das **Record** -Objekt stellt eine Entität dar, die mit einer URL nicht angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="22422-125">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="22422-126">Die Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="22422-126">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="22422-p104">[!HINWEIS] Diese Eigenschaft wird nur von Dokumentquellenanbietern wie z. B. [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) unterstützt. Weitere Informationen finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="22422-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="22422-129">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der Microsoft OLE DB Provider für Internet Publishing automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22422-129">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="22422-130">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="22422-130">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="22422-131">[!HINWEIS] Enthält der aktuelle Datensatz einen Datensatz aus einem ADO- **Recordset** -Objekt, verursacht der Zugriff auf die **ParentURL** -Eigenschaft einen Laufzeitfehler, der angibt, dass keine URL möglich ist.</span><span class="sxs-lookup"><span data-stu-id="22422-131">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>



---
<span data-ttu-id="39afe-101"><<<<<<< HEAD-Titel: HelpContext- und HelpFile-Eigenschaften (ADO) TOCTitle: HelpContext-und HelpFile-Eigenschaften (ADO) Ms:assetid: 8a79f994-f17c-2983-0593-095801be762e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) Ms:contentKeyID: 48546194 ms.date: 09/18 / 2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="39afe-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="39afe-102">HelpContext- und HelpFile-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="39afe-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="39afe-103">=== Titel: HelpContext-und HelpFile-Eigenschaft (ADO) TOCTitle: HelpContext-und HelpFile-Eigenschaft (ADO) Ms:assetid: 8a79f994-f17c-2983-0593-095801be762e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) Ms:contentKeyID: 48546194 ms.date: 10/17/2018 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="39afe-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="39afe-104">HelpContext-und HelpFile-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="39afe-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="39afe-105">master</span><span class="sxs-lookup"><span data-stu-id="39afe-105">master</span></span>

<span data-ttu-id="39afe-106">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="39afe-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="39afe-107">Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="39afe-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="39afe-108"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="39afe-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="39afe-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="39afe-109">Return Values</span></span>

  - <span data-ttu-id="39afe-110">**HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.</span><span class="sxs-lookup"><span data-stu-id="39afe-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="39afe-111">**HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="39afe-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="39afe-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="39afe-112">Return values</span></span>

- <span data-ttu-id="39afe-113">**HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.</span><span class="sxs-lookup"><span data-stu-id="39afe-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="39afe-114">**HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="39afe-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="39afe-115">master</span><span class="sxs-lookup"><span data-stu-id="39afe-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="39afe-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39afe-116">Remarks</span></span>

<span data-ttu-id="39afe-p101">Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="39afe-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>


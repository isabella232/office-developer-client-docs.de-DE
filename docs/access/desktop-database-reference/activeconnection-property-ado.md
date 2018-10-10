---
title: ActiveConnection-Eigenschaft (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476074"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="3a293-102">ActiveConnection-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a293-102">ActiveConnection Property (ADO)</span></span>


<span data-ttu-id="3a293-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a293-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a293-104">Gibt an, zu welchem [Connection](connection-object-ado.md)-Objekt das angegebene [Command](command-object-ado.md)-, [Recordset](recordset-object-ado.md)- oder [Record](record-object-ado.md)-Objekt derzeit gehört.</span><span class="sxs-lookup"><span data-stu-id="3a293-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3a293-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3a293-105">Settings and Return Values</span></span>

<span data-ttu-id="3a293-p101">Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** zurückgegeben oder festgelegt, der eine Definition für eine Verbindung enthält, falls die Verbindung geschlossen ist, oder ein Wert vom Datentyp **Variant**, der das aktuelle **Connection** -Objekt enthält, falls die Verbindung geöffnet ist. Der Standard ist ein nullwertiger Objektverweis. Siehe [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3a293-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a293-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a293-109">Remarks</span></span>

<span data-ttu-id="3a293-110">Bestimmen Sie mithilfe der **ActiveConnection** -Eigenschaft das **Connection** -Objekt, über das das angegebene **Command** -Objekt ausgeführt oder das angegebene **Recordset** -Objekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3a293-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

<span data-ttu-id="3a293-111">**Command**</span><span class="sxs-lookup"><span data-stu-id="3a293-111">**Command**</span></span>

<span data-ttu-id="3a293-112">Für **Command** -Objekte weist die **ActiveConnection** -Eigenschaft Lese-/Schreibzugriff auf.</span><span class="sxs-lookup"><span data-stu-id="3a293-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="3a293-113">Ein Fehler wird erzeugt, wenn Sie die [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))-Methode für ein **Command** -Objekt aufrufen, bevor Sie diese Eigenschaft auf ein geöffnetes **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="3a293-113">If you attempt to call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="3a293-114">**Microsoft Visual Basic** Festlegen der **ActiveConnection** -Eigenschaft auf *Nothing* das **Command** -Objekt aus der aktuellen **Verbindung** trennt und bewirkt, dass den Anbieter keine zugeordneten Ressourcen für die Datenquelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="3a293-114">**Microsoft Visual Basic**Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="3a293-115">Sie können dann das **Command** -Objekt demselben oder einem anderen **Connection** -Objekt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3a293-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="3a293-116">Einige Anbieter können Sie die Einstellung der Eigenschaft aus eine **Verbindung** zu einem anderen zu ändern, ohne dass zuerst die-Eigenschaft auf *Nothing*festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a293-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="3a293-117">Wenn die [Parameters](parameters-collection-ado.md) -Auflistung des **Command** -Objekts vom Anbieter bereitgestellte Parameter enthält, wird die Auflistung gelöscht, wenn Sie die **ActiveConnection** -Eigenschaft auf *Nothing* oder zu einer anderen **Connection** -Objekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a293-117">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object.</span></span> <span data-ttu-id="3a293-118">Wenn Sie manuell [Parameter](parameter-object-ado.md) -Objekte erstellen und diese zum Füllen der **Parameters** -Auflistung des **Command** -Objekts verwenden, bewirkt, dass durch Festlegen der **ActiveConnection** -Eigenschaft auf *Nothing* oder zu einer anderen **Connection** -Objekt die **Parameters** -Auflistung erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="3a293-118">If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="3a293-p104">Durch Schließen des **Connection**-Objekts, dem ein **Command**-Objekt zugeordnet ist, wird die **ActiveConnection**-Eigenschaft auf *Nothing* festgelegt. Ein Fehler wird generiert, wenn Sie diese Eigenschaft auf ein geschlossenes **Connection**-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="3a293-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

<span data-ttu-id="3a293-121">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="3a293-121">**Recordset**</span></span>

<span data-ttu-id="3a293-p105">Für geöffnete **Recordset** -Objekte oder für **Recordset** -Objekte, deren [Source](source-property-ado-recordset.md)-Eigenschaft auf ein gültiges **Command** -Objekt festgelegt ist, ist die **ActiveConnection** -Eigenschaft schreibgeschützt. Andernfalls weist sie Lese-/Schreibzugriff auf.</span><span class="sxs-lookup"><span data-stu-id="3a293-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="3a293-p106">Sie können für diese Eigenschaft ein gültiges **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festlegen. In diesem Fall erstellt der Anbieter mithilfe dieser Definition ein neues **Connection** -Objekt und öffnet die Verbindung. Darüber hinaus kann der Anbieter diese Eigenschaft auf ein neues **Connection** -Objekt festlegen, um Ihnen eine Möglichkeit für den Zugriff auf das **Connection** -Objekt zu bieten, damit Sie erweiterte Fehlerinformationen abrufen oder andere Befehle ausführen können.</span><span class="sxs-lookup"><span data-stu-id="3a293-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="3a293-127">Wenn Sie das Argument *ActiveConnection* der [Open](open-method-ado-recordset.md) -Methode verwenden, um ein **Recordset** -Objekt zu öffnen, erbt die **ActiveConnection** -Eigenschaft den Wert des Arguments.</span><span class="sxs-lookup"><span data-stu-id="3a293-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="3a293-128">Wenn Sie die **Source** -Eigenschaft des **Recordset** -Objekts auf eine gültige **Command** -Objektvariable festlegen, erbt die **ActiveConnection** -Eigenschaft des **Recordset** -Objekts die Einstellung der **ActiveConnection** -Eigenschaft des **Command** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a293-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="3a293-129">**Remote Data Service-Verwendung** Wenn für ein clientseitiges Recordset-Objekt verwendet wird, kann diese Eigenschaft nur für eine Verbindungszeichenfolge oder (in Microsoft Visual Basic oder Visual Basic Scripting Edition) auf *Nothing*festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3a293-129">**Remote Data Service Usage**When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

<span data-ttu-id="3a293-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="3a293-130">**Record**</span></span>

<span data-ttu-id="3a293-p107">Diese Eigenschaft weist Lese-/Schreibzugriff auf, wenn das **Record** -Objekt geschlossen ist, und kann eine Verbindungszeichenfolge oder einen Verweis auf ein geöffnetes **Connection** -Objekt enthalten. Diese Eigenschaft ist schreibgeschützt, wenn das **Record** -Objekt geöffnet ist, und enthält einen Verweis auf ein geöffnetes **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a293-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="3a293-p108">Ein **Connection** -Objekt wird implizit erstellt, wenn das **Record** -Objekt über eine URL geöffnet wird. Öffnen Sie das **Record** -Objekt mit einem vorhandenen, geöffneten **Connection** -Objekt, indem Sie dem **Connection** -Objekt diese Eigenschaft zuweisen, oder mithilfe des **Connection** -Objekts als Parameter im Aufruf der [Open](open-method-ado-record.md)-Methode. Falls das **Record** -Objekt aus einem vorhandenen **Record** - oder [Recordset](recordset-object-ado.md)-Objekt geöffnet wird, wird es automatisch dem **Connection** -Objekt dieses **Record** - oder **Recordset** -Objekts zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3a293-p108">A **Connection** object is created implicitly when the **Record** object is opened from a URL. Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call. If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), then it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3a293-p109">[!HINWEIS] Für URLs, die das HTTP-Schema verwenden, wird automatisch der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</A> aufgerufen. Weitere Informationen finden Sie unter <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="3a293-p109">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>



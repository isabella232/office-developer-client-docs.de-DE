---
title: Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 582b0e836edc361d1d8717f94a5d7490c57cd530
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719464"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="16b67-102">Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher</span><span class="sxs-lookup"><span data-stu-id="16b67-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="16b67-103">Dieses Thema enthält zwei Codebeispiele, die zeigen, wie die einem Speicher zugeordnete globale Adressliste (GAL) bzw. alle einem Speicher zugeordneten Adresslisten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="16b67-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="16b67-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="16b67-104">Example</span></span>

<span data-ttu-id="16b67-105">In einer Microsoft Outlook-Sitzung, bei der mehrere Microsoft Exchange-Konten im Profil definiert sind, können einem Speicher mehrere Adresslisten zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="16b67-105">In an Outlook session where multiple Exchange accounts are defined in the profile, there can be multiple address lists associated with a store.</span></span> <span data-ttu-id="16b67-106">In den folgenden Codebeispielen geht es jeweils um den Speicher für den aktuellen Ordner, der im aktiven Explorer angezeigt wird. Der Algorithmus zum Abrufen einer globalen Adressliste oder einer Menge von [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\))-Objekten für einen Speicher gilt jedoch für jeden beliebigen Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="16b67-106">In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="16b67-107">Im ersten Codebeispiel ist die DisplayGlobalAddressListForStore-Methode und die GetGlobalAddressList-Funktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="16b67-107">The first code example contains the DisplayGlobalAddressListForStore method and the GetGlobalAddressList function.</span></span> <span data-ttu-id="16b67-108">Die DisplayGlobalAddressListForStore-Methode zeigt im Dialogfeld **Namen auswählen** die globale Adressliste an, die dem aktuellen Speicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16b67-108">The DisplayGlobalAddressListForStore method displays, in the **Select Names** dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="16b67-109">DisplayGlobalAddressListForStore ruft zunächst den aktuellen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="16b67-109">DisplayGlobalAddressListForStore first obtains the current store.</span></span> <span data-ttu-id="16b67-110">Handelt es sich dabei um einen Exchange-Speicher, wird GetGlobalAddressList aufgerufen, um die dem aktuellen Speicher zugeordnete globale Adressliste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16b67-110">If the current store is an Exchange store, GetGlobalAddressList is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="16b67-111">GetGlobalAddressList verwendet das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt und die MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x3D150102, um die PR\_EMSMDB\_SECTION\_UID-Eigenschaft einer Adressliste und den aktuellen Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16b67-111">GetGlobalAddressList uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the MAPI property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list and the current store.</span></span> <span data-ttu-id="16b67-112">GetGlobalAddressList identifiziert eine Adressliste als einem Speicher zugeordnet, wenn ihre PR\_EMSMDB\_SECTION\_UID-Eigenschaften übereinstimmen, und die Adressliste ist die globale Adressliste, wenn ihre [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\))-Eigenschaft [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)) lautet.</span><span class="sxs-lookup"><span data-stu-id="16b67-112">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and the address list is the Global Address List if its [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) property is [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span></span> <span data-ttu-id="16b67-113">Ist der Aufruf von GetGlobalAddressList erfolgreich, zeigt DisplayGlobalAddressListForStore mithilfe des [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\))-Objekts die zurückgegebene globale Adressliste im Dialogfeld **Namen auswählen** an.</span><span class="sxs-lookup"><span data-stu-id="16b67-113">If the call to GetGlobalAddressList succeeds, DisplayGlobalAddressListForStore uses the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the returned Global Address List in the **Select Names** dialog box.</span></span>

<span data-ttu-id="16b67-114">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="16b67-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="16b67-115">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="16b67-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="16b67-116">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="16b67-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

<span data-ttu-id="16b67-117">Das zweite Codebeispiel enthält die EnumerateAddressListsForStore-Methode und die GetAddressLists-Funktion.</span><span class="sxs-lookup"><span data-stu-id="16b67-117">The second code example contains the EnumerateAddressListsForStore method and GetAddressLists function.</span></span> <span data-ttu-id="16b67-118">Die EnumerateAddressListsForStore-Methode zeigt den Typ und die Auflösungsreihenfolge jeder für den aktuellen Speicher definierten Adressliste an.</span><span class="sxs-lookup"><span data-stu-id="16b67-118">The EnumerateAddressListsForStore method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="16b67-119">EnumerateAddressListsForStore ruft zuerst den aktuellen Speicher ab und ruft dann GetAddressLists auf, um ein generisches [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19)-Objekt von .NET Framework abzurufen, das AddressList-Objekte für den aktuellen Speicher enthält.</span><span class="sxs-lookup"><span data-stu-id="16b67-119">EnumerateAddressListsForStore first obtains the current store, and then calls GetAddressLists to obtain a .NET Framework generic [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19) object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="16b67-120">GetAddressLists zählt jede für die Sitzung definierte Adressliste auf und verwendet das PropertyAccessor-Objekt und die benannte MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x3D150102, um die PR\_EMSMDB\_SECTION\_UID-Eigenschaft einer Adressliste und die PR\_EMSMDB\_SECTION\_UID-Eigenschaft eines aktuellen Speichers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16b67-120">GetAddressLists enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property https://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list, and the PR\_EMSMDB\_SECTION\_UID property of a current store.</span></span> <span data-ttu-id="16b67-121">GetGlobalAddressList identifiziert eine Adressliste als einem Speicher zugeordnet, wenn ihre PR\_EMSMDB\_SECTION\_UID-Eigenschaften übereinstimmen, und gibt eine Menge von Adresslisten für den aktuellen Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="16b67-121">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="16b67-122">Anschließend verwendet EnumerateAddressListsForStore die Eigenschaften [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) und [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) des **AddressList**-Objekts, um den Typ und die Auflösungsreihenfolge für jede zurückgegebene Adressliste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16b67-122">EnumerateAddressListsForStore then uses the [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) and [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) properties of the **AddressList** object to display the type and resolution order for each returned address list.</span></span>

```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a><span data-ttu-id="16b67-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16b67-123">See also</span></span>

- [<span data-ttu-id="16b67-124">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="16b67-124">Address book</span></span>](address-book.md)


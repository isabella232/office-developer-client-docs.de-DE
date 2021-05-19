---
title: Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store
ms:contentKeyID: 55119800
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f0f7ba9b8854603646dc41e1017c2465c4af2d8
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819329"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher

Dieses Thema enthält zwei Codebeispiele, die zeigen, wie die einem Speicher zugeordnete globale Adressliste (GAL) bzw. alle einem Speicher zugeordneten Adresslisten abgerufen werden.

## <a name="example"></a>Beispiel

In einer Microsoft Outlook-Sitzung, bei der mehrere Microsoft Exchange-Konten im Profil definiert sind, können einem Speicher mehrere Adresslisten zugeordnet sein. In den folgenden Codebeispielen geht es jeweils um den Speicher für den aktuellen Ordner, der im aktiven Explorer angezeigt wird. Der Algorithmus zum Abrufen einer globalen Adressliste oder einer Menge von [AddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist?redirectedfrom=MSDN&view=outlook-pia)-Objekten für einen Speicher gilt jedoch für jeden beliebigen Exchange-Speicher.

Im ersten Codebeispiel ist die DisplayGlobalAddressListForStore-Methode und die GetGlobalAddressList-Funktion enthalten. Die DisplayGlobalAddressListForStore-Methode zeigt im Dialogfeld **Namen auswählen** die globale Adressliste an, die dem aktuellen Speicher zugeordnet ist. DisplayGlobalAddressListForStore ruft zunächst den aktuellen Speicher ab. Handelt es sich dabei um einen Exchange-Speicher, wird GetGlobalAddressList aufgerufen, um die dem aktuellen Speicher zugeordnete globale Adressliste abzurufen. 

GetGlobalAddressList verwendet das [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)-Objekt und die MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x3D150102, um die PR\_EMSMDB\_SECTION\_UID-Eigenschaft einer Adressliste und den aktuellen Speicher abzurufen. GetGlobalAddressList identifiziert eine Adressliste als einem Speicher zugeordnet, wenn ihre PR\_EMSMDB\_SECTION\_UID-Eigenschaften übereinstimmen, und die Adressliste ist die globale Adressliste, wenn ihre [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType)-Eigenschaft [olExchangeGlobalAddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype?redirectedfrom=MSDN&view=outlook-pia) lautet. Wenn der Aufruf von GetGlobalAddressList erfolgreich ist, verwendet DisplayGlobalAddressListForStore das [SelectNamesDialog]( -Objekt, um die zurückgegebene globale Adressliste im Dialogfeld Namen auswählen https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog?redirectedfrom=MSDN&view=outlook-pia\) anzuzeigen. 

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

Das zweite Codebeispiel enthält die EnumerateAddressListsForStore-Methode und die GetAddressLists-Funktion. Die EnumerateAddressListsForStore-Methode zeigt den Typ und die Auflösungsreihenfolge jeder für den aktuellen Speicher definierten Adressliste an. EnumerateAddressListsForStore ruft zuerst den aktuellen Speicher ab und ruft dann GetAddressLists auf, um ein generisches [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.8)-Objekt von .NET Framework abzurufen, das AddressList-Objekte für den aktuellen Speicher enthält. 

GetAddressLists zählt jede für die Sitzung definierte Adressliste auf und verwendet das PropertyAccessor-Objekt und die benannte MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x3D150102, um die PR\_EMSMDB\_SECTION\_UID-Eigenschaft einer Adressliste und die PR\_EMSMDB\_SECTION\_UID-Eigenschaft eines aktuellen Speichers abzurufen. GetGlobalAddressList identifiziert eine Adressliste als einem Speicher zugeordnet, wenn ihre PR\_EMSMDB\_SECTION\_UID-Eigenschaften übereinstimmen, und gibt eine Menge von Adresslisten für den aktuellen Speicher zurück. Anschließend verwendet EnumerateAddressListsForStore die Eigenschaften [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) und [ResolutionOrder](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_ResolutionOrder) des **AddressList**-Objekts, um den Typ und die Auflösungsreihenfolge für jede zurückgegebene Adressliste anzuzeigen.


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
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

## <a name="see-also"></a>Siehe auch

- [Adressbuch](address-book.md)


---
title: Charset-Eigenschaft (ADO)
TOCTitle: Charset Property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84436f814bbc2a503e843d4e9832fa2bab612b58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475393"
---
# <a name="charset-property-ado"></a><span data-ttu-id="8444f-102">Charset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8444f-102">Charset Property (ADO)</span></span>


<span data-ttu-id="8444f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8444f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8444f-104">Gibt den Zeichensatz an, in den der Inhalt eines Textdatenstroms übersetzt werden soll, um ihn im internen Puffer des Stream-Objekts zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8444f-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8444f-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8444f-105">Settings and Return Values</span></span>

<span data-ttu-id="8444f-106">Legt fest oder gibt einen **String** -Wert, der angibt, in den der Inhalt des **Datenstroms** übersetzt werden, werden den Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="8444f-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="8444f-107">Der Standardwert lautet "Unicode".</span><span class="sxs-lookup"><span data-stu-id="8444f-107">The default value is "Unicode".</span></span> <span data-ttu-id="8444f-108">Zulässige Werte sind typische Zeichenfolgen, die über die Schnittstelle übergeben, wie Internet-Zeichenfolgen Zeichensatz (z. B. "Iso-8859-1", "Windows-1252" Etc.).</span><span class="sxs-lookup"><span data-stu-id="8444f-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="8444f-109">Eine Liste mit den Satz Zeichenfolgen, die von einem System bekannt ist, finden Sie unter der Unterschlüssel des HKEY\_Klassen\_ROOT\\MIME\\Datenbank\\Charset in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="8444f-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="8444f-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8444f-110">Remarks</span></span>

<span data-ttu-id="8444f-p102">In einem **Stream** -Textobjekt werden Textdaten in dem durch die **Charset** -Eigenschaft angegebenen Zeichensatz gespeichert. Der Standard ist Unicode. Mithilfe der **Charset** -Eigenschaft werden Daten konvertiert, die an das **Stream** -Objekt übertragen werden oder vom **Stream** -Objekt ausgehen. Wenn z. B. das **Stream** -Objekt ISO-8859-1-Daten enthält und diese zu einem BSTR kopiert werden, konvertiert das **Stream** -Objekt die Daten in Unicode. Dies gilt auch im umgekehrten Fall.</span><span class="sxs-lookup"><span data-stu-id="8444f-p102">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property. The default is Unicode. The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**. For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode. The reverse is also true.</span></span>

<span data-ttu-id="8444f-116">Für ein geöffnetes **Stream** -Objekt muss die aktuelle [Position](position-property-ado.md) am Beginn des **Stream** -Objekts (0) sein, damit **Charset** festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8444f-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="8444f-p103">**Charset** wird nur für **Stream**-Textobjekte ([Type](type-property-ado-stream.md) ist **adTypeText**) verwendet. Diese Eigenschaft wird ignoriert, wenn **Type** gleich **adTypeBinary** ist.</span><span class="sxs-lookup"><span data-stu-id="8444f-p103">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>


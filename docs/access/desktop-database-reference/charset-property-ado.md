---
title: CharSet-Eigenschaft (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296388"
---
# <a name="charset-property-ado"></a>CharSet-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated. The default value is "Unicode". Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.). Eine Liste der Zeichensatz Zeichenfolgen, die von einem System bekannt sind, finden Sie unter\_Schlüssel der HKEY-Klassen\_Stamm\\-\\MIME\\-Datenbankzeichensatz in der Windows-Registrierung.

## <a name="remarks"></a>Bemerkungen

In einem **Stream**-Textobjekt werden Textdaten in dem durch die **Charset**-Eigenschaft angegebenen Zeichensatz gespeichert. Der Standard ist Unicode. Mithilfe der **Charset**-Eigenschaft werden Daten konvertiert, die an das **Stream**-Objekt übertragen werden oder vom **Stream**-Objekt ausgehen. Wenn z. B. das **Stream**-Objekt ISO-8859-1-Daten enthält und diese zu einem BSTR kopiert werden, konvertiert das **Stream**-Objekt die Daten in Unicode. Dies gilt auch im umgekehrten Fall.

Für ein geöffnetes **Stream**-Objekt muss die aktuelle [Position](position-property-ado.md) am Beginn des **Stream**-Objekts (0) sein, damit **Charset** festgelegt werden kann.

**Charset** wird nur für **Stream**-Textobjekte ([Type](type-property-ado-stream.md) ist **adTypeText**) verwendet. Diese Eigenschaft wird ignoriert, wenn **Type** gleich **adTypeBinary** ist.


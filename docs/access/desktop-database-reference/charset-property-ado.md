---
title: Charset-Eigenschaft (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca38e10402a8353d6a32a8cd288bd72ce4ec60e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562832"
---
# <a name="charset-property-ado"></a>Charset-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated. The default value is "Unicode". Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.). Eine Liste der Zeichensatzzeichenfolgen, die einem System bekannt sind, finden Sie unter den Unterschlüsseln von HKEY \_ CLASSES ROOT MIME Database \_ \\ \\ \\ Charset in der Windows Registry.

## <a name="remarks"></a>HinwBemerkungeneise

In einem **Stream**-Textobjekt werden Textdaten in dem durch die **Charset**-Eigenschaft angegebenen Zeichensatz gespeichert. Der Standard ist Unicode. Mithilfe der **Charset**-Eigenschaft werden Daten konvertiert, die an das **Stream**-Objekt übertragen werden oder vom **Stream**-Objekt ausgehen. Wenn z. B. das **Stream**-Objekt ISO-8859-1-Daten enthält und diese zu einem BSTR kopiert werden, konvertiert das **Stream**-Objekt die Daten in Unicode. Dies gilt auch im umgekehrten Fall.

Für ein geöffnetes **Stream**-Objekt muss die aktuelle [Position](position-property-ado.md) am Beginn des **Stream**-Objekts (0) sein, damit **Charset** festgelegt werden kann.

**Charset** wird nur für **Stream**-Textobjekte ([Type](type-property-ado-stream.md) ist **adTypeText**) verwendet. Diese Eigenschaft wird ignoriert, wenn **Type** gleich **adTypeBinary** ist.


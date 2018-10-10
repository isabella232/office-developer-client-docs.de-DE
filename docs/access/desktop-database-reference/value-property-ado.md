---
title: Value-Eigenschaft (ADO)
TOCTitle: Value Property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68c0d45345dfc768f5d435689abf67bcc3d9abe2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472884"
---
# <a name="value-property-ado"></a>Value-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Wert an, der einem [Field](field-object-ado.md)-, [Parameter](parameter-object-ado.md)- oder [Property](property-object-ado.md)-Objekt zugewiesen ist.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Variant** -Wert fest, der den Wert eines Objekts angibt, oder gibt den Wert zurück. Der Standardwert hängt von der [Type](type-property-ado.md)-Eigenschaft ab.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Value** -Eigenschaft zum Festlegen oder Zurückgeben von Daten bei **Field** -Objekten, zum Festlegen oder Zurückgeben von Parameterwerten bei **Parameter** -Objekten oder zum Festlegen oder Zurückgeben von Eigenschafteneinstellungen bei **Property** -Objekten. Ob die **Value** -Eigenschaft schreibgeschützt ist, hängt von verschiedenen Faktoren ab. Weitere Informationen dazu finden Sie in dem Thema zum jeweiligen Objekt.

ADO ermöglicht das Festlegen oder Zurückgeben von Long binary-Daten mit der Value-Eigenschaft.


> [!NOTE]
> <P>[!HINWEIS] Bei <STRONG>Parameter</STRONG> -Objekten liest ADO die <STRONG>Value</STRONG> -Eigenschaft nur einmal vom Anbieter. Wenn ein Befehl ein <STRONG>Parameter</STRONG> -Objekt enthält, dessen <STRONG>Value</STRONG> -Eigenschaft leer ist, und Sie ein <A href="recordset-object-ado.md">Recordset</A>-Objekt durch den Befehl erstellen, schließen Sie zuerst das <STRONG>Recordset</STRONG> -Objekt. Rufen Sie erst danach die <STRONG>Value</STRONG> -Eigenschaft ab. Andernfalls ist bei einigen Anbietern die <STRONG>Value</STRONG> -Eigenschaft möglicherweise leer und enthält nicht den richtigen Wert.</P>



Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, muss die **Value** -Eigenschaft festgelegt werden, bevor andere **Field** -Eigenschaften angegeben werden. Zuerst müssen ein angegebener Wert für die **Value** -Eigenschaft zugewiesen und die [Update](update-method-ado.md)-Methode für die **Fields** -Auflistung aufgerufen worden sein. Anschließend kann auf weitere Eigenschaften, wie z. B. [Type](type-property-ado.md) oder [Attributes](attributes-property-ado.md), zugegriffen werden.


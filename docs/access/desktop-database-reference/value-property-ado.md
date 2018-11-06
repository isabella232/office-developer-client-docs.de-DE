---
title: Value-Eigenschaft (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61803648a0efa5f226b222fb54ce96c8aadbfe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999057"
---
# <a name="value-property-ado"></a>Value-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt den Wert an, der einem [Field](field-object-ado.md)-, [Parameter](parameter-object-ado.md)- oder [Property](property-object-ado.md)-Objekt zugewiesen ist.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Variant** -Wert fest, der den Wert eines Objekts angibt, oder gibt den Wert zurück. Der Standardwert hängt von der [Type](type-property-ado.md)-Eigenschaft ab.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Value** -Eigenschaft zum Festlegen oder Zurückgeben von Daten bei **Field** -Objekten, zum Festlegen oder Zurückgeben von Parameterwerten bei **Parameter** -Objekten oder zum Festlegen oder Zurückgeben von Eigenschafteneinstellungen bei **Property** -Objekten. Ob die **Value** -Eigenschaft schreibgeschützt ist, hängt von verschiedenen Faktoren ab. Weitere Informationen dazu finden Sie in dem Thema zum jeweiligen Objekt.

ADO ermöglicht das Festlegen oder Zurückgeben von Long binary-Daten mit der Value-Eigenschaft.

> [!NOTE]
> [!HINWEIS] Bei **Parameter** -Objekten liest ADO die **Value** -Eigenschaft nur einmal vom Anbieter. Wenn ein Befehl ein **Parameter** -Objekt enthält, dessen **Value** -Eigenschaft leer ist, und Sie ein [Recordset](recordset-object-ado.md)-Objekt durch den Befehl erstellen, schließen Sie zuerst das **Recordset** -Objekt. Rufen Sie erst danach die **Value** -Eigenschaft ab. Andernfalls ist bei einigen Anbietern die **Value** -Eigenschaft möglicherweise leer und enthält nicht den richtigen Wert.

Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, muss die **Value** -Eigenschaft festgelegt werden, bevor andere **Field** -Eigenschaften angegeben werden. Zuerst müssen ein angegebener Wert für die **Value** -Eigenschaft zugewiesen und die [Update](update-method-ado.md)-Methode für die **Fields** -Auflistung aufgerufen worden sein. Anschließend kann auf weitere Eigenschaften, wie z. B. [Type](type-property-ado.md) oder [Attributes](attributes-property-ado.md), zugegriffen werden.


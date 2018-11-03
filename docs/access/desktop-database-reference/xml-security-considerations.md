---
title: Hinweise zur XML-Sicherheit
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23cec1f900d109299e621ccabd30fe34cc54d63f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947340"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="fbec6-102">XML-Sicherheitsaspekte</span><span class="sxs-lookup"><span data-stu-id="fbec6-102">XML security considerations</span></span>


<span data-ttu-id="fbec6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbec6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="fbec6-104">Überlegungen zur Sicherheit bei XML</span><span class="sxs-lookup"><span data-stu-id="fbec6-104">XML Security Considerations</span></span>

<span data-ttu-id="fbec6-p101">Die Methoden **Save** und **Open** von ADO im **Recordset** -Objekt gelten für die Ausführung in Internet Explorer als nicht sicher. Wenn deshalb diese Methoden in Skriptcode verwendet werden, der in einer Anwendung oder einem Steuerelement ausgeführt wird, die bzw. das in einem Browser bereitgestellt wird, wirkt sich die Sicherheitskonfiguration des Browsers auf das Verhalten aus.</span><span class="sxs-lookup"><span data-stu-id="fbec6-p101">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer. Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="fbec6-p102">In Internet Explorer 5 gibt es standardmäßig in den Internetzonen Sicherheitseinschränkungen für solche Vorgänge. Mit dieser Konfiguration hat das **Recordset** -Objekt keinen Zugriff auf das lokale Datensystem auf dem Client sowie keinen Zugriff auf Datenquellen außerhalb der Domäne des Servers, von dem die Seite heruntergeladen wurde. Bei der Ausführung im Browserhost kann ein **Recordset** -Objekt nur in einer Datei gespeichert werden, wenn es sich auf dem Server befindet, von dem die Seite heruntergeladen wurde. Entsprechend können Sie ein **Recordset** -Objekt nur öffnen, indem Sie es aus einer Datei laden, wenn sich diese Datei auf dem Server befindet, von dem die Seite heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="fbec6-p102">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones. Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded. Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded. Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="fbec6-111">Weitere Informationen zur Sicherheit in Internet Explorer finden Sie im technischen Artikel "ADO and RDS Security Issues in Microsoft Internet Explorer" (in englischer Sprache).</span><span class="sxs-lookup"><span data-stu-id="fbec6-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>


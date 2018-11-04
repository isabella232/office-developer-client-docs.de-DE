---
title: WillConnect-Ereignis (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8ac4ab83062d9297483b7ee4883ab0b289af227
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949831"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="a12d8-102">WillConnect-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="a12d8-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="a12d8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a12d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a12d8-104">Das **WillConnect** -Ereignis wird aufgerufen, bevor eine Verbindung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a12d8-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a12d8-105">Syntax</span></span>

<span data-ttu-id="a12d8-106">WillConnect*ConnectionString*, *UserID*, *Kennwort*, *Optionen*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="a12d8-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="a12d8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a12d8-107">Parameters</span></span>

|<span data-ttu-id="a12d8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a12d8-108">Parameter</span></span>|<span data-ttu-id="a12d8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a12d8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a12d8-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="a12d8-110">*ConnectionString*</span></span> |<span data-ttu-id="a12d8-111">Ein **String** -Wert, der Verbindungsinformationen für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="a12d8-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="a12d8-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="a12d8-112">*UserID*</span></span> |<span data-ttu-id="a12d8-113">Ein **String** -Wert, der einen Benutzernamen für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="a12d8-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="a12d8-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="a12d8-114">*Password*</span></span> |<span data-ttu-id="a12d8-115">Ein **String** -Wert, der ein Kennwort für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="a12d8-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="a12d8-116">*Options*</span><span class="sxs-lookup"><span data-stu-id="a12d8-116">*Options*</span></span> |<span data-ttu-id="a12d8-p101">Ein **Long**-Wert, der angibt, wie *ConnectionString* vom Anbieter ausgewertet werden soll. Die einzige Option ist **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="a12d8-p101">A **Long** value that indicates how the provider should evaluate the *ConnectionString*. Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="a12d8-119">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a12d8-119">*adStatus*</span></span> |<span data-ttu-id="a12d8-120">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="a12d8-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="a12d8-121">Beim Aufrufen dieses Ereignisses wird dieser Parameter standardmäßig auf **adStatusOK** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a12d8-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="a12d8-122">Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn das Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="a12d8-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="a12d8-p103">Legen Sie diesen Parameter vor der Rückgabe dieses Ereignisses auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Legen Sie diesen Parameter auf **adStatusCancel** fest, um den Verbindungsvorgang anzufordern, der zum Abbruch dieser Benachrichtigung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="a12d8-p103">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="a12d8-125">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="a12d8-125">*pConnection*</span></span> |<span data-ttu-id="a12d8-p104">Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt. Vom **WillConnect** -Ereignishandler vorgenommene Änderungen an den Parametern des **Connection** -Objekts haben keine Auswirkungen auf das **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a12d8-p104">The [Connection](connection-object-ado.md) object for which this event notification applies. Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a12d8-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a12d8-128">Remarks</span></span>

<span data-ttu-id="a12d8-p105">Wenn **WillConnect** aufgerufen wird, werden für die Parameter *ConnectionString*, *UserID*, *Password* und *Options* die Werte festgelegt, die durch den dieses Ereignis verursachenden Vorgang (die ausstehende Verbindung) bestimmt wurden. Die Parameter können vor der Rückgabe des Ereignisses geändert werden. Von **WillConnect** kann möglicherweise eine Anforderung zurückgegeben werden, dass die ausstehende Verbindung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a12d8-p105">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns. **WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="a12d8-131">Wenn dieses Ereignis abgebrochen wird, wird mit den *AdStatus* -Parameter auf **AdStatusErrorsOccurred**festgelegt **ConnectComplete** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a12d8-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>


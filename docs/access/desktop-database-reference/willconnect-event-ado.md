---
title: WillConnect-Ereignis (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51d9d0b11d137fbca8bf5efdddfe51469642c405
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887173"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="bd628-102">WillConnect-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd628-102">WillConnect Event (ADO)</span></span>


<span data-ttu-id="bd628-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd628-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bd628-104">Das **WillConnect** -Ereignis wird aufgerufen, bevor eine Verbindung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="bd628-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd628-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd628-105">Syntax</span></span>

<span data-ttu-id="bd628-106">WillConnect*ConnectionString*, *UserID*, *Kennwort*, *Optionen*, *AdStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="bd628-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="bd628-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd628-107">Parameters</span></span>

  - <span data-ttu-id="bd628-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="bd628-108">*ConnectionString*</span></span>

  - <span data-ttu-id="bd628-109">Ein **String** -Wert, der Verbindungsinformationen für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="bd628-109">A **String** that contains connection information for the pending connection.</span></span>

  - <span data-ttu-id="bd628-110">*UserID*</span><span class="sxs-lookup"><span data-stu-id="bd628-110">*UserID*</span></span>

  - <span data-ttu-id="bd628-111">Ein **String** -Wert, der einen Benutzernamen für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="bd628-111">A **String** that contains a user name for the pending connection.</span></span>

  - <span data-ttu-id="bd628-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="bd628-112">*Password*</span></span>

  - <span data-ttu-id="bd628-113">Ein **String** -Wert, der ein Kennwort für die ausstehende Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="bd628-113">A **String** that contains a password for the pending connection.</span></span>

  - <span data-ttu-id="bd628-114">*Options*</span><span class="sxs-lookup"><span data-stu-id="bd628-114">*Options*</span></span>

  - <span data-ttu-id="bd628-p101">Ein **Long**-Wert, der angibt, wie *ConnectionString* vom Anbieter ausgewertet werden soll. Die einzige Option ist **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="bd628-p101">A **Long** value that indicates how the provider should evaluate the *ConnectionString*. Your only option is **adAsyncOpen**.</span></span>

  - <span data-ttu-id="bd628-117">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="bd628-117">*adStatus*</span></span>

  - [<span data-ttu-id="bd628-118">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="bd628-118">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="bd628-p102">Beim Aufrufen dieses Ereignisses wird dieser Parameter standardmäßig auf **adStatusOK** festgelegt. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn das Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="bd628-p102">When this event is called, this parameter is set to **adStatusOK** by default. It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="bd628-p103">Legen Sie diesen Parameter vor der Rückgabe dieses Ereignisses auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern. Legen Sie diesen Parameter auf **adStatusCancel** fest, um den Verbindungsvorgang anzufordern, der zum Abbruch dieser Benachrichtigung geführt hat.</span><span class="sxs-lookup"><span data-stu-id="bd628-p103">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>

  - <span data-ttu-id="bd628-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="bd628-123">*pConnection*</span></span>

  - <span data-ttu-id="bd628-p104">Das [Connection](connection-object-ado.md)-Objekt, für das diese Ereignisbenachrichtigung gilt. Vom **WillConnect** -Ereignishandler vorgenommene Änderungen an den Parametern des **Connection** -Objekts haben keine Auswirkungen auf das **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd628-p104">The [Connection](connection-object-ado.md) object for which this event notification applies. Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd628-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd628-126">Remarks</span></span>

<span data-ttu-id="bd628-p105">Wenn **WillConnect** aufgerufen wird, werden für die Parameter *ConnectionString*, *UserID*, *Password* und *Options* die Werte festgelegt, die durch den dieses Ereignis verursachenden Vorgang (die ausstehende Verbindung) bestimmt wurden. Die Parameter können vor der Rückgabe des Ereignisses geändert werden. Von **WillConnect** kann möglicherweise eine Anforderung zurückgegeben werden, dass die ausstehende Verbindung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="bd628-p105">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns. **WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="bd628-129">Wenn dieses Ereignis abgebrochen wird, wird mit den *AdStatus* -Parameter auf **AdStatusErrorsOccurred**festgelegt **ConnectComplete** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bd628-129">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>


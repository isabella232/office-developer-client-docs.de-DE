---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Gibt den Konto Stempel des Kontos zurück, das die Nachricht übermittelt hat.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327727"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="eb0fc-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="eb0fc-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="eb0fc-104">Gibt den Konto Stempel des Kontos zurück, das die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eb0fc-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="eb0fc-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb0fc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb0fc-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="eb0fc-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="eb0fc-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="eb0fc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="eb0fc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="eb0fc-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="eb0fc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eb0fc-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="eb0fc-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="eb0fc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="eb0fc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb0fc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eb0fc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-114">Area:</span></span>  <br/> |<span data-ttu-id="eb0fc-115">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="eb0fc-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb0fc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb0fc-116">Remarks</span></span>

<span data-ttu-id="eb0fc-117">Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Account Management API-Eigenschaft [PROP_ACCT_STAMP](prop_acct_stamp.md) für das Konto zurückgegeben wird, das die Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="eb0fc-118">Nachrichtenspeicher Anbieter setzen diese benannte Eigenschaft und [pidlidinternetaccountname (](pidlidinternetaccountname.md) so fest, dass die folgenden Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="eb0fc-119">Wenn ein Benutzer auf **alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die dem Konto zugeordnet ist, und wird auf die Nachricht aus der Empfängerliste der Antwort gestempelt.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="eb0fc-120">Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse ist der Absender der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="eb0fc-121">Standardmäßig sendet Outlook Antworten und weitergeleitete Nachrichten über das Konto, das auf die ursprüngliche Nachricht gestempelt ist.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="eb0fc-122">In der Regel übermittelt der Outlook-Protokoll-Manager Nachrichten, und Outlook legt die Eigenschaften **pidlidinternetaccountname (** und **pidlidinternetaccountstamp (** fest, um das Konto anzugeben, das die Nachricht zugestellt hat.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="eb0fc-123">Wenn jedoch ein Nachrichtenspeicher eng mit einem Transport verbunden ist, stellt der Outlook-Protokoll-Manager keine Nachrichten bereit, und Outlook kann diese Eigenschaften nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="eb0fc-124">In diesem Szenario ruft Outlook die [IMAPIProp:: GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="eb0fc-125">Wenn der Nachrichtenspeicher Anbieter diese benannten Eigenschaften verfügbar machen möchte, sollte er **IMAPIProp:: GetIDsFromNames** implementieren und Eigenschaftstags über den Ausgabeparameter *lppPropTags* zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="eb0fc-126">Outlook kann dann die [IMAPIProp::](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) GetProps-Methode mithilfe dieser Eigenschaftstags aufrufen, und der Nachrichtenspeicher Anbieter kann den Kontonamen und den Stempel des gewünschten Kontos zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="eb0fc-127">Zur Unterstützung dieser benannten Eigenschaften sollten Speicheranbieter davon ausgehen, dass Outlook **IMAPIProp:: GetIDsFromNames** zum Abrufen des Eigenschaftentags für diese Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="eb0fc-128">Outlook gibt die folgenden Werte für die [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur an, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays übergeben wird, auf das durch den Eingabeparameter *lppPropNames* von **IMAPIProp:: GetIDsFromNames**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eb0fc-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb0fc-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="eb0fc-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="eb0fc-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="eb0fc-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-131">ulKind:</span></span>  <br/> |<span data-ttu-id="eb0fc-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="eb0fc-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="eb0fc-133">Art. lID:</span><span class="sxs-lookup"><span data-stu-id="eb0fc-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="eb0fc-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="eb0fc-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb0fc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb0fc-135">See also</span></span>

- [<span data-ttu-id="eb0fc-136">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="eb0fc-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="eb0fc-137">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="eb0fc-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="eb0fc-138">Kanonische Pidlidinternetaccountstamp (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eb0fc-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)


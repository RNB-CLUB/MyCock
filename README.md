
# **This my cock**
![](https://gorodskayaferma.ru/upload/webp/medialibrary/cbe/dhcalfoe56r3peevxymwn7ak3visc43m.webp)
## My name is Sahibjohn. I'm gold **digger**, and i love cocks!
* [OnlyFans](https://onlyfans.com/sosamuzik300) | [TikTok](https://www.tiktok.com/@nivnixxi)
* [Pinterest](https://ru.pinterest.com/pin/215821007146153318/) | [YouTube](https://www.youtube.com/watch?v=aAkMkVFwAoo)
```ts
type UserStatus = 
  | { type: 'Active', lastSeen: Date }
  | { type: 'Away', reason: string, since: Date }
  | { type: 'Offline' };

  const displayStatus = (status: UserStatus): string => {
      switch (status.type) {
          case 'Active':
              const timeAgo = (Date.now() - status.lastSeen.getTime()) / 1000;
      return `🟢 Active (seen ${Math.round(timeAgo)}s ago)`;

    case 'Away':
        return `🟡 Away: ${status.reason} (since ${status.since.toLocaleDateString()})`;

    case 'Offline':
        return `⚫ Offline`;
      
    default:
        const check: never = status;
        return `Unknown status: ${check}`;
  }
};

const currentUser = { 
    name: "Alex", 
    status: { type: 'Active', lastSeen: new Date() } 
} as const;

console.log(`${currentUser.name} is ${displayStatus(currentUser.status)}`);
```
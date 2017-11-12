```Json
Person: {
  id: 12314,
  user_id: 10000, 
  conditions: {
    health: 50,
    maxHealth:50,
    stamina: 100,
    maxStamina: 100
  },
  status: [
    {buff or debuff object}
  ],
  belogings: [物品对象数组],
  equipments: {
    head: {物品对象},
    face: {},
    chest: {},
    leftArm: {},
    rightArm: {},
    leftHand: {},
    rightHand: {},
    waist: {},
    leftLeg: {},
    rightLeg: {},
    leftFoot: {},
    rightFoot: {}
  },
  attributes: {
    str: 5,
    dex: 5,
    con: 5,
    int: 5,
    wis: 5,
    cha: 5 
  },
  skills: [
      {技能对象}
  ]
}
```
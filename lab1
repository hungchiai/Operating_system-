# Operating_system-

#include <linux/module.h>
#include <linux/init.h>
#include <linux/moduleparam.h>
#include <linux/kernel.h>


static int level = 3;
module_param(level, int, S_IRUGO);
MODULE_PARM_DESC(level, "Log level (0-7)");


static int __init lab1_init(void)
{
    
    switch(level) {
        case 0:
            printk(KERN_EMERG "[INIT] Log level: KERN_EMERG\n");
            break;
        case 1:
            printk(KERN_ALERT "[INIT] Log level: KERN_ALERT\n");
            break;
        case 2:
            printk(KERN_CRIT "[INIT] Log level: KERN_CRIT\n");
            break;
        case 3:
            printk(KERN_ERR "[INIT] Log level: KERN_ERR\n");
            break;
        case 4:
            printk(KERN_WARNING "[INIT] Log level: KERN_WARNING\n");
            break;
        case 5:
            printk(KERN_NOTICE "[INIT] Log level: KERN_NOTICE\n");
            break;
        case 6:
            printk(KERN_INFO "[INIT] Log level: KERN_INFO\n");
            break;
        case 7:
            printk(KERN_DEBUG "[INIT] Log level: KERN_DEBUG\n");
            break;
        default:
            printk(KERN_ERR "[INIT] Invalid level %d, using default KERN_ERR\n", level);
            level = 3;
            break;
    }
   
    return 0;
}


static void __exit lab1_exit(void)
{
    
    switch(level) {
        case 0:
            printk(KERN_EMERG "KERN_EMERG[EXIT] Module_removed at level %d\n", level);
            break;
        case 1:
            printk(KERN_ALERT "KERN_ALERT[EXIT] Module_removed at level %d\n", level);
            break;
        case 2:
            printk(KERN_CRIT "KERN_CRIT[EXIT] Module_removed at level %d\n", level);
            break;
        case 3:
            printk(KERN_ERR "KERN_ERR[EXIT] Module_removed at level %d\n", level);
            break;
        case 4:
            printk(KERN_WARNING "KERN_WARNING[EXIT] Module_removed at level %d\n", level);
            break;
        case 5:
            printk(KERN_NOTICE "KERN_NOTICE[EXIT] Module_removed at level %d\n", level);
            break;
        case 6:
            printk(KERN_INFO "KERN_INFO[EXIT] Module_removed at level %d\n", level);
            break;
        case 7:
            printk(KERN_DEBUG "KERN_DEBUG[EXIT] Module_removed at level %d\n", level);
            break;
        default:
            printk(KERN_ERR "KERN_ERR[EXIT] Module_removed at level %d\n", level);
            break;
    }
}

module_init(lab1_init);
module_exit(lab1_exit);

MODULE_LICENSE("GPL");
MODULE_AUTHOR("Student");
MODULE_DESCRIPTION("A kernel module with configurable log level parameter");
MODULE_VERSION("1.0");
